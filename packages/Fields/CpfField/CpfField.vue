<template>
	<mask-field mask="###.###.###-##" :masked="masked" :value="value" @input="$emit('input',$event)" v-bind="$attrs" />
</template>

<script>
	import MaskField from '../MaskField/MaskField.vue'
	export default {
		name:"CpfField",
		components: { MaskField },
		props: {
			value: String,
			masked: {
				// by default emits the value unformatted, change to true to format with the mask
				type: Boolean,
				default: false // raw
			},
		},
	}
</script>

<style>

</style>