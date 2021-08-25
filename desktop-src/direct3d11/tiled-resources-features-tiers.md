---
title: Livelli di funzionalità delle risorse affiancate
description: Direct3D 11.2 espone il supporto delle risorse affiancate in due livelli con i valori D3D11 \_ TILED \_ RESOURCES \_ TIER.
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b76c1d90cc48210f02983817b317eb830224b8f87bb8b4904ee3e11d6cdd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894381"
---
# <a name="tiled-resources-features-tiers"></a>Livelli di funzionalità delle risorse affiancate

Direct3D 11.2 espone il supporto delle risorse affiancate in due livelli con i valori [**D3D11 \_ TILED \_ RESOURCES \_ TIER.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier)

Per verificare se l'hardware e il driver supportano le risorse affiancate e a quale livello, passare il valore [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) al parametro *Feature* di [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Passare inoltre un puntatore alla struttura [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) al parametro *pFeatureSupportData* e passare le dimensioni della struttura **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS1** *al parametro FeatureSupportDataSize.* **CheckFeatureSupport** restituisce il livello come valore [**D3D11 \_ TILED \_ RESOURCES \_ TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) nel membro **TiledResourcesTier** di **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS1.**

Questa sezione descrive questi due livelli.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                           | Descrizione                                       |
|---------------------------------|---------------------------------------------------|
| [Livello 1](tier-1.md)<br/> | Questa sezione descrive il supporto di livello 1.<br/> |
| [Livello 2](tier-2.md)<br/> | Questa sezione descrive il supporto di livello 2.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 





