---
description: Sebbene i termini Width e pitch siano spesso utilizzati in modo informale, presentano significati molto importanti e distinti. Di conseguenza, è necessario comprendere i significati per ciascuno di essi e come interpretare i valori utilizzati da Direct3D per descriverli.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Spessore rispetto a pitch (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50d0c8fc49b3bce984e56f7b1a727ed40fee67b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104561884"
---
# <a name="width-vs-pitch-direct3d-9"></a>Spessore rispetto a pitch (Direct3D 9)

Sebbene i termini Width e pitch siano spesso utilizzati in modo informale, presentano significati molto importanti e distinti. Di conseguenza, è necessario comprendere i significati per ciascuno di essi e come interpretare i valori utilizzati da Direct3D per descriverli.

Direct3D usa la struttura [**D3DSURFACE \_ desc**](d3dsurface-desc.md) per includere le informazioni che descrivono una superficie. Tra le altre cose, questa struttura è definita per contenere informazioni sulle dimensioni di una superficie, nonché sul modo in cui tali dimensioni sono rappresentate in memoria. La struttura usa i membri Height e Width per descrivere le dimensioni logiche della superficie. Entrambi i membri sono misurati in pixel. Pertanto, i valori di altezza e larghezza per una superficie 640 x 480 sono gli stessi se si tratta di una superficie a 8 bit o di una superficie RGB a 24 bit.

Quando si blocca una superficie usando il metodo [**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , il metodo compila una struttura [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) che contiene il pitch della superficie e un puntatore ai bit bloccati. Il valore nel membro pitch descrive il passo di memoria della superficie, detto anche stride. Pitch è la distanza in byte tra due indirizzi di memoria che rappresentano l'inizio di una riga bitmap e l'inizio della riga bitmap successiva. Poiché il pitch viene misurato in byte anziché in pixel, una superficie 640x480x8 presenta un valore di pitch molto diverso rispetto a una superficie con le stesse dimensioni ma un formato pixel diverso. Inoltre, il valore di pitch riflette talvolta i byte che Direct3D ha riservato come cache, quindi non è sicuro presupporre che il pitch sia solo la larghezza moltiplicata per il numero di byte per pixel. È invece possibile visualizzare la differenza tra Width e pitch, come illustrato nella figura seguente.

![diagramma del passo e della larghezza per lo stesso buffer anteriore, buffer nascosto e cache](images/pitch.png)

In questo diagramma, il buffer anteriore e il buffer nascosto sono entrambi 640x480x8 e la cache è 384x480x8.

Quando si accede direttamente alle superfici, prestare attenzione a rimanere nella memoria allocata per le dimensioni della superficie e rimanere in memoria riservata alla cache. Inoltre, quando si blocca solo una parte di una superficie, è necessario rimanere all'interno del rettangolo specificato durante il blocco della superficie. Il mancato completamento di queste linee guida avrà risultati imprevedibili. Quando si esegue il rendering direttamente nella memoria della superficie, usare sempre il pitch restituito dal metodo [**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) . Non presupporre un pitch basato esclusivamente sulla modalità di visualizzazione. Se l'applicazione funziona su alcune schede di visualizzazione ma sembra distorta dagli altri, questa potrebbe essere la causa del problema.

Per ulteriori informazioni, vedere [accesso diretto alla memoria di Surface (Direct3D 9)](accessing-surface-memory-directly.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
