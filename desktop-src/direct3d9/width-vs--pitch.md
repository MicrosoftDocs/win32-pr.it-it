---
description: Anche se i termini larghezza e passo vengono spesso usati in modo informale, hanno significati molto importanti e distinti. Di conseguenza, è necessario comprendere i significati per ognuno di essi e come interpretare i valori utilizzati da Direct3D per descriverli.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Larghezza e passo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1c697ec4c9278a78a5539818b30038d99fc9d59d96af7f22ee87c33949abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095516"
---
# <a name="width-vs-pitch-direct3d-9"></a>Larghezza e passo (Direct3D 9)

Anche se i termini larghezza e passo vengono spesso usati in modo informale, hanno significati molto importanti e distinti. Di conseguenza, è necessario comprendere i significati per ognuno di essi e come interpretare i valori utilizzati da Direct3D per descriverli.

Direct3D usa la [**struttura \_ DESC D3DSURFACE**](d3dsurface-desc.md) per portare informazioni che descrivono una superficie. Tra le altre cose, questa struttura è definita per contenere informazioni sulle dimensioni di una superficie e sul modo in cui tali dimensioni vengono rappresentate in memoria. La struttura usa i membri Height e Width per descrivere le dimensioni logiche della superficie. Entrambi i membri sono misurati in pixel. Di conseguenza, i valori di Altezza e Larghezza per una superficie 640 x 480 sono gli stessi se si tratta di una superficie a 8 bit o di una superficie RGB a 24 bit.

Quando si blocca una superficie usando il metodo [**IDirect3DSurface9::LockRect,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) il metodo riempie una struttura [**D3DLOCKED \_ RECT**](d3dlocked-rect.md) che contiene l'altezza della superficie e un puntatore ai bit bloccati. Il valore nel membro Pitch descrive l'andatura della memoria della superficie, detta anche stride. Il passo è la distanza, in byte, tra due indirizzi di memoria che rappresentano l'inizio di una riga della bitmap e l'inizio della riga della bitmap successiva. Poiché il passo viene misurato in byte anziché in pixel, una superficie 640x480x8 ha un valore di passo molto diverso rispetto a una superficie con le stesse dimensioni ma un formato pixel diverso. Inoltre, il valore dell'intonazione talvolta riflette i byte che Direct3D ha riservato come cache, quindi non è sicuro presupporre che il passo sia solo la larghezza moltiplicata per il numero di byte per pixel. Visualizzare invece la differenza tra larghezza e passo, come illustrato nel diagramma seguente.

![diagramma dell'altezza e della larghezza per lo stesso front buffer, buffer nascosto e cache](images/pitch.png)

In questo diagramma il front buffer e il buffer nascosto sono entrambi 640x480x8 e la cache è 384x480x8.

Quando si accede direttamente alle superfici, fare attenzione a rimanere all'interno della memoria allocata per le dimensioni della superficie e rimanere fuori dalla memoria riservata per la cache. Inoltre, quando si blocca solo una parte di una superficie, è necessario rimanere all'interno del rettangolo specificato quando si blocca la superficie. La mancata applicazione di queste linee guida avrà risultati imprevedibili. Quando si esegue il rendering direttamente nella memoria surface, usare sempre il passo restituito dal [**metodo IDirect3DSurface9::LockRect.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) Non presupporre un passo basato esclusivamente sulla modalità di visualizzazione. Se l'applicazione funziona su alcune schede video, ma sembra non essere compatibile con altre, questa potrebbe essere la causa del problema.

Per altre informazioni, vedere [Accesso diretto a Surface Memory (Direct3D 9).](accessing-surface-memory-directly.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
