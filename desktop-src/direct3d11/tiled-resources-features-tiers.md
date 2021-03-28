---
title: Livelli di funzionalità delle risorse affiancate
description: Direct3D 11,2 espone il supporto di risorse affiancate in due livelli con i \_ valori del livello di risorse affiancati d3d11 \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955224"
---
# <a name="tiled-resources-features-tiers"></a>Livelli di funzionalità delle risorse affiancate

Direct3D 11,2 espone il supporto di risorse affiancate in due livelli con i valori del [**\_ \_ \_ livello di risorse affiancati d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .

Per eseguire una query per determinare se l'hardware e il driver supportano le risorse affiancate e a quale livello di livello, passare la [**\_ funzionalità d3d11 \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) valore al parametro *feature* di [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Inoltre, passare un puntatore alla struttura [**d3d11 \_ \_ data \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) al parametro *pFeatureSupportData* e passare la dimensione **della struttura d3d11 d3d11 OPTIONS1 al parametro \_ \_ \_ \_** *FeatureSupportDataSize* . **CheckFeatureSupport** restituisce il livello di livello come valore del [**\_ \_ \_ livello di risorse affiancato d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) nel membro **TiledResourcesTier** dei **dati della \_ funzionalità d3d11 \_ \_ d3d11 \_** OPTIONS1.

In questa sezione vengono descritti questi due livelli.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                           | Descrizione                                       |
|---------------------------------|---------------------------------------------------|
| [Livello 1](tier-1.md)<br/> | In questa sezione viene descritto il supporto di livello 1.<br/> |
| [Livello 2](tier-2.md)<br/> | In questa sezione viene descritto il supporto di livello 2.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 





