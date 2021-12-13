<template>
  <b-row class="pt-2">
    <b-col cols="3" class="px-0">
      <b-card
        no-body
        bg-variant="info"
        text-variant="light"
        class="p-2 text-center"
      >
        <b-card-body>
          <h2>Jacob Brookins</h2>
          <p class="m-auto">Software Engineer</p>
          <p class="m-auto">Seattle, WA</p>
        </b-card-body>
      </b-card>
      <b-card bg-variant="info" text-variant="light">
        <b-card-title>Contact Information</b-card-title>
        <p>
          Phone:
          <b-link class="link-light" href="tel:+17706885088" v-if="showPhone">
            +1 (770) 688-5088</b-link
          >
        </p>
        <p>
          Email:
          <b-link
            class="link-light"
            href="mailto:jacob@brookins.email"
            v-if="showEmail"
            >jacob@brookins.email</b-link
          >
        </p>
        <div class="text-center h3">
          <b-link
            class="link-light"
            href="https://www.linkedin.com/in/wbrookins/"
            target="_blank"
            ><b-icon-linkedin></b-icon-linkedin
          ></b-link>
          <b-link
            class="link-light"
            target="_blank"
            href="https://github.com/jdogwilly"
            ><b-icon-github></b-icon-github
          ></b-link>
        </div>
      </b-card>
      <b-card bg-variant="info" text-variant="light">
        <b-card-title>Skills</b-card-title>
        <b-card-body>
          <h6>Languages</h6>
          <b-badge pill class="bg-secondary">C++</b-badge>
          <b-badge pill class="bg-secondary">Python</b-badge>
          <b-badge pill class="bg-secondary">Java</b-badge>
          <b-badge pill class="bg-secondary">Typescript</b-badge>
          <h6 class="mt-3">Technologies</h6>
          <b-badge pill class="bg-warning">AWS</b-badge>
          <b-badge pill class="bg-secondary">CDK</b-badge>
          <b-badge pill class="bg-secondary">CI/CD</b-badge>
          <b-badge pill class="bg-secondary"></b-badge>
        </b-card-body>
      </b-card>
    </b-col>
    <b-col cols="9" class="px-0">
      <b-card v-if="blurbs">
        <b-card-text>
          <p v-for="blurb in blurbs">{{ blurb }}</p>
        </b-card-text>
      </b-card>
      <b-card>
        <b-card-title>Experience</b-card-title>
        <hr />
        <item-entry
          endDate="Now"
          startDate="March 2020"
          mainTitle="Software Development Engineer, Amazon.com"
          subtitle="Seattle, Washington, United States"
          v-bind:bulletPoints="[
            'Work on teams that enable the earth\'s largest catalog',
            'Maintained and Operationally supported systems that serve billions of requests',
            'Mentored an intern and new team members',
          ]"
        />
        <item-entry
          endDate="July 2019"
          startDate="May 2019"
          mainTitle="Software Development Engineer Intern, Amazon.com"
          subtitle="Seattle, Washington, United States"
          v-bind:bulletPoints="[
            'Studied user feedback related to a diagnostic too',
            'Designed a shcema for persisting diagnostic runs',
          ]"
        />
        <item-entry
          endDate="August 2018"
          startDate="June 2018"
          mainTitle="Software Development Engineer Intern, Amazon.com"
          subtitle="Seattle, Washington, United States"
          v-bind:bulletPoints="[
            'Worked to add a new portal to an internal tool',
            'Spring Java Backend and React Typescript Frontend',
            'Designed the tool based on an understanding of my team\'s overall architecture',
            'Deployed my changes into Production',
          ]"
        />
        <item-entry
          endDate="Now"
          startDate="August 2015"
          mainTitle="Head of IT, Doctor Electric, Inc."
          subtitle="Atlanta, Georgia, United States"
          v-bind:bulletPoints="[
            'Develop serverless cloud applications to automate tasks',
            'Advise on IT strategy and helped with organizational goals',
            'Designed cloud based alternatives to legacy software to reduce overhead',
          ]"
        />
      </b-card>
      <b-card>
        <b-card-title>Education</b-card-title>
        <hr />
        <item-entry
          endDate="December 2019"
          startDate="August 2014"
          mainTitle="Bachelors of Computer Science, The University of Alabama"
          subtitle="Tuscaloosa, Alabama, United States"
          v-bind:bulletPoints="[
            'Minor in Mathematics',
            'Coursework in Embedded Systems, Algorithms, and Software Engineering',
            'Spent 2 years in a working group upgrading labs and designed a data collection system',
          ]"
        />
      </b-card>
      <b-card>
        <b-card-title>Volunteering</b-card-title>
        <hr />
        <b-card-text>
          <h4 class="mb-auto">2020 Amazon Future Engineer Hackathon</h4>
          <p>
            Assisted as a technical consultant for an internal hackathon put on
            for Amazon Future Engineer Students.
          </p>
        </b-card-text>
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: {
    blurbs: Array,
    showPhone: Boolean,
    showEmail: Boolean,
  },
}
</script>
