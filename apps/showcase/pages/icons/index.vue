<template>
    <div>
        <Head>
            <Title>OpenIcons - OpenVue</Title>
            <Meta name="description" content="OpenIcons is the default icon library of OpenVue with over 250 open source icons. OpenIcons is optional as OpenVue components can use any icon with templating." />
        </Head>

        <div class="doc">
            <div class="doc-main">
                <div class="doc-intro">
                    <div class="flex flex-col sm:flex-row sm:items-start sm:justify-between gap-4 mb-4">
                        <div class="flex-1">
                            <h1>Icons</h1>
                            <p>
                                <a href="https://github.com/openvi-foundation/openicons" target="_blank" rel="noopener noreferrer">OpenIcons</a>
                                is the default icon library of OpenVue with over 250 open source icons maintained by the OpenVi Foundation. OpenIcons is optional as OpenVue components can use any icon with templating.
                            </p>
                        </div>
                        <DocCopyMarkdown docType="page" class="flex-shrink-0" />
                    </div>
                </div>
                <DocSections :docs="docs" />
            </div>
            <DocSectionNav :docs="docs" />
        </div>
    </div>
</template>

<script>
import DocCopyMarkdown from '@/components/doc/DocCopyMarkdown.vue';
import BasicDoc from '@/doc/icons/BasicDoc.vue';
import ColorDoc from '@/doc/icons/ColorDoc.vue';
import CompatibilityDoc from '@/doc/icons/CompatibilityDoc.vue';
import ConstantsDoc from '@/doc/icons/ConstantsDoc.vue';
import DownloadDoc from '@/doc/icons/DownloadDoc.vue';
import ImportDoc from '@/doc/icons/ImportDoc.vue';
import ListDoc from '@/doc/icons/ListDoc.vue';
import SizeDoc from '@/doc/icons/SizeDoc.vue';
import SpinDoc from '@/doc/icons/SpinDoc.vue';

export default {
    components: { DocCopyMarkdown },
    data() {
        return {
            docs: [
                {
                    id: 'download',
                    label: 'Download',
                    component: DownloadDoc
                },
                {
                    id: 'import',
                    label: 'Import',
                    component: ImportDoc
                },
                {
                    id: 'compatibility',
                    label: 'Compatibility',
                    component: CompatibilityDoc
                },
                {
                    id: 'basic',
                    label: 'Basic',
                    component: BasicDoc
                },
                {
                    id: 'size',
                    label: 'Size',
                    component: SizeDoc
                },
                {
                    id: 'color',
                    label: 'Color',
                    component: ColorDoc
                },
                {
                    id: 'spin',
                    label: 'Spin',
                    component: SpinDoc
                },
                {
                    id: 'constants',
                    label: 'Constants',
                    component: ConstantsDoc
                },
                {
                    id: 'list',
                    label: 'List',
                    component: ListDoc
                }
            ]
        };
    }
};
</script>
