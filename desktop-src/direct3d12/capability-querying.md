---
title: Esecuzione di query sulle funzionalità
description: "L'applicazione può individuare il livello di supporto per l'associazione di risorse e molte altre funzionalità, con una chiamata a ID3D12Device \\: \\: CheckFeatureSupport."
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: eaf451f91d51cfa6e900f328898c3418f0974a2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548806"
---
# <a name="capability-querying"></a>Esecuzione di query sulle funzionalità

L'applicazione può individuare il livello di supporto per l'associazione di risorse (e il livello di supporto per molte altre funzionalità), con una chiamata a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

## <a name="how-to-query-for-the-resource-binding-tier"></a>Come eseguire una query per il livello di associazione delle risorse

Questo primo esempio è incentrato sull'associazione di risorse. Ogni livello di associazione di risorse è un superset dei livelli inferiori della funzionalità, quindi il codice che funziona su un determinato livello funziona senza modifiche su un livello superiore.

I livelli di associazione delle risorse sono costanti nell'enumerazione [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) .

Per eseguire una query per il livello di associazione delle risorse, usare codice simile al seguente. In questo esempio di codice viene illustrato il modello generale per l'esecuzione di query per uno dei diversi tipi di supporto della funzionalità.

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

Si noti che qualsiasi costante enumerata passata ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), in questo caso) ha una struttura di dati corrispondente che riceve informazioni su tale funzionalità o set di funzionalità (in questo caso,[**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)). Passare sempre un puntatore alla struttura che corrisponde alla costante enumerata passata.

## <a name="how-to-query-for-any-feature-level"></a>Come eseguire una query per qualsiasi livello di funzionalità

Oltre al livello di associazione delle risorse, sono disponibili molte altre funzionalità il cui livello di supporto è possibile eseguire query per usando lo stesso modello illustrato nell'esempio di codice precedente. È sufficiente passare una costante diversa dall'enumerazione [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (per indicare all'API quale funzionalità richiedere informazioni di supporto) e passare un puntatore a un'istanza della struttura corrispondente (in cui ricevere le informazioni richieste).

- Passare **D3D12_FEATURE_ARCHITECTURE** e [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Passare **D3D12_FEATURE_ARCHITECTURE1** e [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Passare **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** e [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Passare **D3D12_FEATURE_CROSS_NODE** e [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Passare **D3D12_FEATURE_D3D12_OPTIONS** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Passare **D3D12_FEATURE_D3D12_OPTIONS1** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Passare **D3D12_FEATURE_D3D12_OPTIONS2** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Passare **D3D12_FEATURE_D3D12_OPTIONS3** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Passare **D3D12_FEATURE_D3D12_OPTIONS4** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Passare **D3D12_FEATURE_D3D12_OPTIONS5** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Passare **D3D12_FEATURE_EXISTING_HEAPS** e [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Passare **D3D12_FEATURE_FEATURE_LEVELS** e [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Passare **D3D12_FEATURE_FORMAT_INFO** e [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Passare **D3D12_FEATURE_FORMAT_SUPPORT** e [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Passare **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** e [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Passare **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** e [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Passare **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** e [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Passare **D3D12_FEATURE_ROOT_SIGNATURE** e [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Passare **D3D12_FEATURE_SERIALIZATION** e [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Passare **D3D12_FEATURE_SHADER_CACHE** e [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Passare **D3D12_FEATURE_SHADER_MODEL** e [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Supporto hardware per formati DXGI

Per visualizzare le tabelle dei formati DXGI e delle funzionalità hardware, fare riferimento a questi argomenti.

- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Supporto hardware per i formati 10Level9 Direct3D](/previous-versions//ff471324(v=vs.85))
- [Supporto hardware per formati Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
- [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

* [Binding delle risorse in Direct3D 12](resource-binding.md)
* [Livelli di funzionalità hardware](hardware-feature-levels.md)
* [Firme radice](root-signatures.md)