---
description: Uso delle destinazioni di rendering Direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Uso delle destinazioni di rendering Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7bacf36402b071d60989e225cdcd9533500494a0593bcf9753ddc06bb93ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650341"
---
# <a name="working-with-direct3d-render-targets"></a>Uso delle destinazioni di rendering Direct3D

Diversi sottotipi multimediali per le destinazioni di rendering Direct3D sono definiti per l'uso con VMR-7 e VMR-9. Quando un filtro upstream propone una connessione con uno di questi sottotipi, indica alla macchina virtuale che il rendering deve essere eseguito in una destinazione di rendering Direct3D. Per VMR-7, si tratta di una destinazione di rendering DirectX 7 Direct3D e per VMR-9 sarà una destinazione di rendering DirectX 9 Direct3D. Se la macchina virtuale è in modalità di combinazione, anche la superficie sarà una superficie di trama Direct3D. Se la macchina virtuale non è in modalità di combinazione, la superficie sarà una normale superficie Direct3D. I formati di pixel ARGB sono supportati solo quando la macchina virtuale è in modalità di combinazione. I sottotipi di destinazione di rendering sono:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB44444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB44444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Questi tipi sono definiti nel file di intestazione uuids.h. I tipi di supporti MEDIASUBTYPE RGB32 sono in formato \_ RGBx888 e MEDIASUBTYPE \_ RGB16 sono in formato RGB565. Per altre informazioni su questi formati pixel, vedere la documentazione di DirectX Graphics.

**Richiesta di una superficie sbloccata**

Il blocco e lo sblocco delle superfici DirectDraw sono operazioni dispendiose dal punto di vista del calcolo. Quando si usano i sottotipi di supporti di destinazione del rendering Direct3D, il filtro upstream deve sbloccare le superfici in modo che possa operare su di essi con l'hardware grafico. Per evitare un'operazione di blocco-sblocco non necessaria, la macchina virtuale supporta un nuovo flag nel metodo [**IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) AM \_ GBF NODDSURFACELOCK, che indica alla macchina virtuale di non bloccare la superficie DirectDraw prima di passare un campione al filtro \_ upstream. Quando viene usato questo flag, le chiamate a [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) avranno esito negativo perché non è presente alcun puntatore bloccato. Per ottenere l'accesso alla superficie directdraw, il filtro deve chiamare **QueryInterface** sull'oggetto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) restituito e richiedere [**l'interfaccia IVMRSurface.**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) Ovviamente, il filtro upstream deve garantire che la superficie non venga bloccata quando rilascia l'esempio nell'elenco gratuito.

 

 



