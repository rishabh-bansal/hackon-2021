<template>
  <Container id="about">
    <section class="content-section">
      <HashHeader title="We're ready for 2.0!" />
      <div class="contents">
        <div class="about">
          <p>
            HackOn is a week-long global digital hackathon that is organized by hackers for hackers 
            to bring their ideas from the point of inception to reality. No matter how new or old you 
            may be in the world of hackathons, HackOn has a place for everyone wanting 
            to learn, build, share, and grow in their lives.
          </p>
          <p>
            Learn new technologies, enhance your team management and
            presentation skills, and get mentored by experts- all in one place!
          </p>
          <p>
            Our journey as one of the first leading virtual hackathon started in April 2020 
            at the beginning of the COVID-19 pandemic, where we brought over 2500 hackers 
            from all across India together to solve problems in healthcare, remote lifestyle, 
            and other issues that came with the lockdown. 
          </p>
        </div>
        <div class="stats">
          <div class="gridLayout">
            <div class="statData">
              <h4>2500+</h4>
              <p>Hackers</p>
            </div>
            <div class="statData">
              <h4>500+</h4>
              <p>Hacks</p>
            </div>
            <div class="statData">
              <h4>25+</h4>
              <p>Speakers</p>
            </div>
            <div class="statData">
              <h4>20+</h4>
              <p>Days</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </Container>
</template>

<script>
import Container from "~/components/Container";
import HashHeader from "~/components/HashHeader";

export default {
  components: {
    Container,
    HashHeader
  }
};
</script>

<style lang="scss" scoped>
.content-section {
  display: flex;
  flex-direction: column;
  padding: 40px 0 10px;

  .contents {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 20px;

    @include respond-below(md) {
      grid-template-columns: repeat(1, 1fr);
    }

    .about {
      padding: 10px 0;

      p {
        padding-top: 20px;
      }
    }
  }

  .stats {
    text-align: center;
    justify-content: center;
    padding: 30px 0 10px;

    .gridLayout {
      display: grid;
      margin-top: 15px;
      grid-template-columns: repeat(2, 180px);
      column-gap: 10px;
      row-gap: 10px;
      justify-content: center;

      @include respond-below(sm) {
        grid-template-columns: repeat(2, 150px);
      }
    }

    .statData {
      height: 150px;
      width: 150px;
      margin: 0;
      display: flex;
      flex-direction: column;
      text-align: center;
      justify-content: center;
      padding: 15px;
      background: var(--color-secondary-light);
      border-radius: 8px;

      h4 {
        font-size: 2rem;
        font-weight: bold;
        padding-bottom: 10px;
      }

      @include respond-below(sm) {
        width: 120px;
        height: 120px;
      }
    }
  }
}
</style>
