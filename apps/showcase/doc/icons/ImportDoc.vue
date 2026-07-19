<template>
    <DocSectionText v-bind="$attrs">
        <p>CSS file of the icon library needs to be imported at the entry point of your application.</p>
    </DocSectionText>
    <DocSectionCode :code="code" hideToggleCode importCode hideStackBlitz />
</template>

<script>
export default {
    data() {
        return {
            code: {
                basic: "\nimport '@openvue/openicons/openicons.css'\n"
            }
        };
    }
};
</script>
