---
title: Mapping trame predefinito
description: L'uso del mapping trame predefinito riduce la copia e l'utilizzo della memoria durante la condivisione dei dati di immagine tra la GPU e la CPU.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc81fc1bf59a974f9bd901fc96d43afc16019edce68fbaabfbf3259c0d4a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752291"
---
# <a name="default-texture-mapping"></a>Mapping trame predefinito

L'uso del mapping trame predefinito riduce la copia e l'utilizzo della memoria durante la condivisione dei dati di immagine tra la GPU e la CPU. Tuttavia, deve essere usato solo in situazioni specifiche. Il layout a scorrimento standard evita di copiare o scorrere i dati in più layout.

-   [Overview](#overview)
-   [API D3D11.3](#d3d113-apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Il mapping delle trame predefinite non deve essere la prima scelta per gli sviluppatori. Gli sviluppatori devono prima codificare in modo discreto-GPU, ovvero non hanno accesso alla CPU per la maggior parte delle trame e caricano con [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1). Tuttavia, in alcuni casi, la CPU e la GPU possono interagire così frequentemente sugli stessi dati, che il mapping delle trame predefinite diventa utile per risparmiare energia o per velocizzare una progettazione specifica su schede o architetture specifiche. Le applicazioni devono rilevare questi casi e ottimizzare le copie non necessarie.

In D3D11.3 le trame create con D3D11 TEXTURE LAYOUT UNDEFINED (un membro dell'enumerazione \_ \_ \_ [**D3D11 \_ TEXTURE \_ LAYOUT)**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) e nessun accesso alla CPU sono le più efficienti per il rendering e il campionamento frequenti della GPU. Durante i test delle prestazioni, queste trame devono essere confrontate con D3D11 TEXTURE LAYOUT UNDEFINED con accesso \_ \_ alla CPU e \_ D3D11 \_ TEXTURE LAYOUT \_ 64K STANDARD SWIZZLE con accesso alla CPU e \_ \_ \_ D3D11 TEXTURE LAYOUT ROW \_ MAJOR \_ \_ \_ per il supporto tra adattatori.

L'uso di LAYOUT TEXTURE D3D11 UNDEFINED con accesso ALLA CPU consente ai metodi \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource), [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (che preclude l'accesso dell'applicazione al puntatore) e [**Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap), ma può sacrificare l'efficienza dell'accesso alla GPU. L'uso di D3D11 \_ TEXTURE \_ LAYOUT 64K STANDARD SWIZZLE con accesso alla CPU abilita \_ \_ \_ **WriteToSubresource**, **ReadFromSubresource**, **Map** (che restituisce un puntatore valido all'applicazione) e Unmap . Può anche sacrificare l'efficienza dell'accesso alla GPU più di D3D11 \_ TEXTURE \_ LAYOUT \_ UNDEFINED con accesso alla CPU.

In generale, le applicazioni devono creare la maggior parte delle trame come accessibili solo tramite GPU e con LAYOUT DI TRAMA D3D11 \_ \_ \_ UNDEFINED.

Prima della funzionalità di mapping delle trame predefinite, esisteva un solo layout standardizzato per i dati multidimensionali: "lineare", noto anche come "row-major". Le applicazioni devono evitare le trame DINAMICHE \_ USAGE STAGING e USAGE quando è disponibile \_ l'impostazione predefinita della mappa. Le trame DINAMICHE USAGE \_ STAGING e USAGE usano il layout \_ lineare.

D3D11.3 (e D3D12) introducono un layout di dati multidimensionale standard. Questa operazione viene eseguita per consentire a più unità di elaborazione di operare sugli stessi dati senza copiare i dati o scorrere i dati tra più layout. Un layout standardizzato consente di migliorare l'efficienza tramite gli effetti di rete e consente agli algoritmi di eseguire brevi riduzioni presupponendo un modello specifico.

Si noti tuttavia che questo girello standard è una funzionalità hardware e potrebbe non essere supportato da tutte le GPU.

## <a name="d3d113-apis"></a>API D3D11.3

A differenza di D3D12, D3D11.3 non supporta il mapping trame per impostazione predefinita, pertanto è necessario eseguire una query [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2). Sarà anche necessario eseguire query su Swizzle Standard con una chiamata a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) e controllando il campo `StandardSwizzle64KBSupported` **di D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**.

Le API seguenti fanno riferimento al mapping delle trame:

Enumerazioni

-   [**D3D11 \_ LAYOUT \_ TRAMA:**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) controlla il modello di scorrimento delle trame predefinite e abilita il supporto della mappa per le trame predefinite.
-   [**D3D11 \_ FEATURE:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) fa [**riferimento a D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3D11 \_ TILE \_ COPY \_ FLAG:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) contiene flag per copiare le risorse affiancate con scorrimento in e da buffer lineari.

Strutture

-   [**D3D11 \_ TEXTURE2D \_ DESC1:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) descrive una trama 2D. Si noti la struttura helper CD3D11 \_ TEXTURE2D \_ DESC1.
-   [**D3D11 \_ TEXTURE3D \_ DESC1:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) descrive una trama 3D. Si noti la struttura helper CD3D11 \_ TEXTURE3D \_ DESC1.

Metodi

-   [**ID3D11Device3::CreateTexture2D1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) crea una matrice di trame 2D.
-   [**ID3D11Device3::CreateTexture3D1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) crea una singola trama 3D.
-   [**ID3D11Device3::WriteToSubresource:**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) copia i dati in una trama D3D11 USAGE DEFAULT mappata \_ \_ tramite [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11Device3::ReadFromSubresource:**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) copia i dati da una trama D3D11 USAGE DEFAULT mappata \_ \_ tramite [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11DeviceContext::Map:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) ottiene un puntatore ai dati contenuti in una sottorisorsa e nega alla GPU l'accesso a tale sottorisorsa.
-   [**ID3D11DeviceContext::Unmap:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) invalida il puntatore a una risorsa e riabilita l'accesso della GPU a tale risorsa.
-   [**ID3D11Texture2D1::GetDesc1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) ottiene le proprietà di una risorsa trama 2D.
-   [**ID3D11Texture3D1::GetDesc1:**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) ottiene le proprietà di una risorsa trama 3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11.3](direct3d-11-3-features.md)
</dt> </dl>

 

 




