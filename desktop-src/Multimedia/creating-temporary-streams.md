---
title: Creazione di flussi temporanei
description: Creazione di flussi temporanei
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate (funzione)
- AVIStreamRelease (funzione)
- AVIMakeCompressedStream (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471195"
---
# <a name="creating-temporary-streams"></a>Creazione di flussi temporanei

I flussi temporanei possono essere utili in diversi modi. È possibile usare un flusso temporaneo come flusso di lavoro, ad esempio quando si modifica il formato del flusso. In alternativa, è possibile creare un flusso temporaneo per contenere parti di altri flussi che sono stati copiati.

È possibile creare un flusso in memoria non associato ad alcun file tramite la funzione [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) . Questa funzione restituisce l'indirizzo dell'interfaccia al nuovo flusso in una posizione specificata e viene usato internamente da altre funzioni che creano flussi temporanei.

È possibile creare un flusso compresso da un flusso non compresso usando la funzione [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) . Si identifica il flusso da comprimere, il metodo di compressione e le opzioni di compressione e il gestore per il nuovo flusso.

Al termine dell'uso di un flusso creato con **AVIStreamCreate** o **AVIMakeCompressedStream**, chiudere il flusso usando la funzione [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . **AVIStreamRelease** libera le risorse usate dal flusso temporaneo.

 

 




