<template>
  <doc-section id="affix" name="Affix">
    <div class="bs-example">
      <h3>
        The sub-navigation on the RIGHT is a live demo of the affix.
        <spam class="visible-xs-block visible-sm-block">(The live demo is hidden in small screens)</spam>
        <tooltip trigger="hover" effect="fadein" content="I'm a direction, not jerking off!" placement="left">
          <span class="glyphicon glyphicon-hand-right pull-right animated shake hidden-xs hidden-sm"></span>
        </tooltip>
      </h3>
    </div>
    <doc-code language="markup">
      <affix offset="50">
        <ul>
          <li>...</li>
          <li>...</li>
          <li>...</li>
        </ul>
        <a href="#">...</a>
      </affix>
    </doc-code>
    <doc-options>
      <div>
        <p>offset</p>
        <p><code>Number</code></p>
        <p><code>0</code></p>
        <p>Pixels to offset from top of screen when calculating position of scroll.</p>
      </div>
    </doc-options>
  </doc-section>
</template>

<script>
import docSection from './docSection.vue'
import docOptions from './docOptions.vue'
import docCode from './docCode.vue'
import tooltip from 'src/Tooltip.vue'

export default {
  components: {
    docSection,
    docOptions,
    docCode,
    tooltip
  }
}
</script>

<style>
.animated {
    -webkit-animation-duration: 3s;
    animation-duration: 3s;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    animation-iteration-count: infinite
}
@keyframes shake {
    0%, 100% {transform: translateX(0);}
    10%, 30%, 50%, 70%, 90% {transform: translateX(-5px);}
    20%, 40%, 60%, 80% {transform: translateX(5px);}
}
.shake {
    -webkit-animation-name: shake;
    animation-name: shake;
}
</style>
