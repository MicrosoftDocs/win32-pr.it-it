---
description: Utilizzo delle destinazioni di rendering Direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Utilizzo delle destinazioni di rendering Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8aca19082c5db9521cfc1c7341fd74c98270cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308938"
---
# <a name="working-with-direct3d-render-targets"></a>Utilizzo delle destinazioni di rendering Direct3D

Diversi sottotipi di supporti per le destinazioni di rendering Direct3D vengono definiti per l'uso con VMR-7 e VMR-9. Quando un filtro upstream propone una connessione con uno di questi sottotipi, indica a VMR che il rendering deve essere eseguito su una destinazione di rendering Direct3D. Per VMR-7, si tratta di una destinazione di rendering Direct3D DirectX 7 e per VMR-9 si tratta di una destinazione di rendering Direct3D DirectX 9. Se il VMR è in modalità di combinazione, la superficie sarà anche una superficie di trama Direct3D. Se VMR non è in modalità di combinazione, la superficie sarà una normale superficie Direct3D. I formati di pixel ARGB sono supportati solo quando VMR è in modalità di combinazione. I sottotipi di destinazione di rendering sono:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ rgb32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ rgb32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ rgb16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ rgb16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Questi tipi sono definiti nel file di intestazione UUIDs. h. I \_ tipi di supporto MEDIASUBTYPE rgb32 sono un formato RGBx888 e MEDIASUBTYPE i \_ tipi di supporto rgb16 sono un formato RGB565. Per ulteriori informazioni su questi formati pixel, vedere la documentazione di DirectX Graphics.

**Richiesta di una superficie sbloccata**

Il blocco e lo sblocco delle superfici DirectDraw sono operazioni costose dal punto di vista del calcolo. Quando si usano i sottotipi di supporto per il rendering Direct3D, il filtro upstream richiede che le superfici vengano sbloccate in modo da poterle usare con l'hardware grafico. Per evitare un'operazione non necessaria di sblocco del blocco, VMR supporta un nuovo flag nel metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , am \_ GBF \_ NODDSURFACELOCK, che indica al VMR di non bloccare la superficie DirectDraw prima di passare un campione al filtro upstream. Quando si usa questo flag, le chiamate a [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) avranno esito negativo perché non è presente alcun puntatore bloccato. Per ottenere l'accesso alla superficie DirectDraw, il filtro deve chiamare **QueryInterface** sull'oggetto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) restituito e richiedere l'interfaccia [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Ovviamente, il filtro upstream deve garantire che la superficie non venga bloccata quando rilascia l'esempio nell'elenco di disponibilità.

 

 



