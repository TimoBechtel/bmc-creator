<div class="canvas">
  {#each topBoxes as box}
    <div class={box.class}>
      <h2>{box.title}</h2>
      <p contenteditable="true">{box.text}</p>
    </div>
  {/each}
  <div class="bottom">
    {#each bottomBoxes as box}
      <div class={box.class}>
        <h2>{box.title}</h2>
        <p contenteditable="true">{box.text}</p>
      </div>
    {/each}
  </div>
</div>

<script>
  const topBoxes = [
    {
      title: '🤝 Key Partners',
      text: `In order to optimize operations and reduce risks of a business model,
        organizations usually cultivate buyer-supplier relationships so they can
        focus on their core activity. Complementary business alliances also can
        be considered through joint ventures or strategic alliances between
        competitors or non-competitors.`,
      class: 'key-partners',
    },
    {
      title: '🏃‍♀️ Key Activities',
      text: ` The most important activities in executing a company's value
        proposition. An example for Bic, the pen manufacturer, would be creating
        an efficient supply chain to drive down costs.`,
      class: 'key-activities',
    },
    {
      title: '🛒 Key Resources',
      text: `The resources that are necessary to create value for the customer. They
        are considered assets to a company that are needed to sustain and
        support the business. These resources could be human, financial,
        physical and intellectual.`,
      class: 'key-resources',
    },
    {
      title: '🎁 Value Propositions',
      text: `The collection of products and services a business offers to meet the
        needs of its customers. According to Osterwalder (2004), a company's
        value proposition is what distinguishes it from its competitors. The
        value proposition provides value through various elements such as
        newness, performance, customization, "getting the job done", design,
        brand/status, price, cost reduction, risk reduction, accessibility, and
        convenience/usability.`,
      class: 'value-proposition',
    },
    {
      title: '💕 Customer Relations',
      text: `To ensure the survival and success of any businesses, companies must
        identify the type of relationship they want to create with their
        customer segments. That element should address three critical steps on a
        customers relationship: How the business will get new customers, how the
        business will keep customers purchasing or using its services and how
        the business will grow its revenue from its current customers.`,
      class: 'customer-relations',
    },
    {
      title: '🚚 Channels',
      text: `A company can deliver its value proposition to its targeted customers
        through different channels. Effective channels will distribute a
        company's value proposition in ways that are fast, efficient and
        cost-effective. An organization can reach its clients through its own
        channels (store front), partner channels (major distributors), or a
        combination of both.`,
      class: 'channels',
    },
    {
      title: '🙋‍♂️ Customer Segments',
      text: `To build an effective business model, a company must identify which
        customers it tries to serve. Various sets of customers can be segmented
        based on their different needs and attributes to ensure appropriate
        implementation of corporate strategy to meet the characteristics of
        selected groups of clients.`,
      class: 'customer-segments',
    },
  ];
  const bottomBoxes = [
    {
      title: '💸 Cost Structure',
      text: `This describes the most important monetary consequences while operating
            under different business models.`,
      class: 'cost-structure',
    },
    {
      title: '💰 Revenue Streams',
      text: `The way a company makes income from each customer segment.`,
      class: 'revenue-streams',
    },
  ];
</script>

<style lang="scss">
  .canvas {
    padding: 20px;
    height: 768px;

    div {
      border: 1px solid var(--color-text-secondary);
      border-radius: 3px;
      padding: 20px;
      p {
        display: block;
        color: var(--color-text-secondary);
        height: 100%;
        outline: none;
      }
    }

    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    gap: 3px 3px;

    .key-partners {
      grid-area: 1 / 1 / 3 / 2;
    }

    .key-activities {
      grid-area: 1 / 2 / 2 / 3;
    }

    .key-resources {
      grid-area: 2 / 2 / 3 / 3;
    }

    .value-proposition {
      grid-area: 1 / 3 / 3 / 4;
    }

    .customer-relations {
      grid-area: 1 / 4 / 2 / 5;
    }

    .channels {
      grid-area: 2 / 4 / 3 / 5;
    }

    .customer-segments {
      grid-area: 1 / 5 / 3 / 6;
    }

    .bottom {
      border: none;
      border-radius: 0;
      padding: 0;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr;
      gap: 3px 3px;
      grid-area: 3 / 1 / 4 / 6;
      .cost-structure {
        grid-area: 1 / 1 / 2 / 2;
      }

      .revenue-streams {
        grid-area: 1 / 2 / 2 / 3;
      }
    }

    @media screen and (max-width: 768px) {
      display: block;
      width: 100%;
      .bottom {
        display: block;
        width: 100%;
      }
    }

    @media print {
      height: 100%;
    }
  }
</style>
