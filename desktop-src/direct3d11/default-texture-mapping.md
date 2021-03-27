---
title: Mapping trama predefinito
description: L'uso del mapping di trama predefinito riduce la copia e l'utilizzo della memoria e condivide i dati di immagine tra la GPU e la CPU.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f203c7590c3673d30315250b2b4ce2663e48c9c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395999"
---
# <a name="default-texture-mapping"></a>Mapping trama predefinito

L'uso del mapping di trama predefinito riduce la copia e l'utilizzo della memoria e condivide i dati di immagine tra la GPU e la CPU. Tuttavia, deve essere usato solo in situazioni specifiche. Il layout swizzle standard evita di copiare o swizzling i dati in più layout.

-   [Overview](#overview)
-   [API di D3D 11.3](#d3d113-apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Il mapping delle trame predefinite non è la prima scelta per gli sviluppatori. Gli sviluppatori devono prima scrivere codice in un modo semplice e intuitivo, ovvero non avere alcun accesso alla CPU per la maggior parte delle trame e caricare con [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1). Tuttavia, per alcuni casi, la CPU e la GPU possono interagire così frequentemente con gli stessi dati, il mapping delle trame predefinite diventa utile per risparmiare energia o per velocizzare una particolare progettazione su specifiche schede o architetture. Le applicazioni devono rilevare questi casi e ottimizzare le copie non necessarie.

In D3D 11.3, le trame create con \_ il layout di trama d3d11 \_ \_ non definito (un membro dell'enumerazione [**\_ \_ layout trama d3d11**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) ) e nessun accesso alla CPU sono le più efficienti per il rendering e il campionamento frequenti della GPU. Quando si esegue il test delle prestazioni, tali trame devono essere confrontate con il layout di trama D3D11 non \_ \_ \_ definito con l'accesso alla CPU e il \_ layout di trama d3d11 \_ \_ 64K \_ standard \_ SWIZZLE con l'accesso alla CPU e \_ \_ la riga del layout della trama d3d11 per il \_ \_ supporto di Cross-adapter.

L'uso del \_ layout di trama d3d11 \_ \_ non definito con l'accesso alla CPU consente ai metodi [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource), [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (che non possono accedere all'applicazione) e [**annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap), ma può sacrificare l'efficienza dell'accesso alla GPU. Usando \_ \_ il layout di trama d3d11 \_ 64K \_ standard \_ SWIZZLE con accesso alla CPU consente **WriteToSubresource**, **ReadFromSubresource**, **Map** (che restituisce un puntatore valido all'applicazione) e **annullare**. Può anche sacrificare l'efficienza dell'accesso alla GPU oltre al layout di trama D3D11 non \_ \_ \_ definito con l'accesso alla CPU.

In generale, le applicazioni devono creare la maggior parte delle trame come accessibili solo per GPU e con layout di trama D3D11 non \_ \_ \_ definito.

Precedente alla funzionalità di mapping delle trame predefinite, era disponibile un solo layout standardizzato per i dati multidimensionali: "lineare", noto anche come "row-major". Le applicazioni devono evitare le \_ trame dinamiche di utilizzo e di gestione temporanea \_ quando è disponibile l'impostazione predefinita della mappa. Le \_ trame dinamiche di utilizzo e di gestione temporanea \_ utilizzano il layout lineare.

D3D 11.3 (e D3D12) introducono un layout standard di dati multidimensionali. Questa operazione viene eseguita per consentire a più unità di elaborazione di operare sugli stessi dati senza copiare i dati o swizzling i dati tra più layout. Un layout standardizzato consente un miglioramento dell'efficienza attraverso gli effetti della rete e consente agli algoritmi di effettuare brevi riduzioni presumendo un modello particolare.

Si noti tuttavia che questa swizzle standard è una funzionalità hardware e potrebbe non essere supportata da tutte le GPU.

## <a name="d3d113-apis"></a>API di D3D 11.3

A differenza di D3D12, D3D 11.3 non supporta il mapping delle trame per impostazione predefinita, pertanto è necessario eseguire una query [**\_ sui dati della funzionalità d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2). Sarà inoltre necessario eseguire query su swizzle standard con una chiamata a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) e controllando il `StandardSwizzle64KBSupported` campo dei **dati della \_ funzionalità \_ d3d11 \_ d3d11 \_** OPTIONS2.

Le API seguenti fanno riferimento al mapping della trama:

Enumerazioni

-   [**D3d11 \_ \_Layout trama**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) : controlla il modello di swizzle delle trame predefinite e Abilita il supporto della mappa sulle trame predefinite.
-   [**D3d11 \_ FUNZIONALITÀ**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) : fa riferimento ai [**\_ dati della funzionalità d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3d11 \_ \_ \_ Flag copia riquadro**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contiene i flag per copiare le risorse swizzled affiancate da e verso buffer lineari.

Strutture

-   [**D3d11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) : descrive una trama 2D. Si noti la \_ \_ struttura Helper CD3D11 TEXTURE2D DESC1.
-   [**D3d11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) : descrive una trama 3D. Si noti la \_ \_ struttura Helper CD3D11 TEXTURE3D DESC1.

Metodi

-   [**ID3D11Device3:: CreateTexture2D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) : crea una matrice di trame 2D.
-   [**ID3D11Device3:: CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) : crea una singola trama 3D.
-   [**ID3D11Device3:: WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) : copia i dati in una \_ trama predefinita di utilizzo d3d11 mappata \_ mediante [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11Device3:: ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) : copia i dati da una trama predefinita di utilizzo di d3d11 mappata \_ \_ mediante [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**Sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) : ottiene un puntatore ai dati contenuti in una sottorisorsa e nega l'accesso alla GPU a tale risorsa.
-   [**Sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) : invalida il puntatore a una risorsa e riabilita l'accesso della GPU a tale risorsa.
-   [**ID3D11Texture2D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) : ottiene le proprietà di una risorsa di trama 2D.
-   [**ID3D11Texture3D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) : ottiene le proprietà di una risorsa di trama 3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




