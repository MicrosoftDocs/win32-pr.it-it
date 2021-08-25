---
title: Creazione di un Flussi
description: Creazione di un Flussi
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Funzione AVIStreamCreate
- Funzione AVIStreamRelease
- Funzione AVIMakeCompressedStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33ce8d4ec6fd88a7283588d35955432cbe01a4855565928dca83d40afa8b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785701"
---
# <a name="creating-temporary-streams"></a>Creazione di un Flussi

I flussi temporanei possono essere utili in diversi modi. È possibile usare un flusso temporaneo come flusso di lavoro, ad esempio quando si modifica il formato del flusso. Oppure è possibile creare un flusso temporaneo per contenere parti di altri flussi copiati.

È possibile creare un flusso in memoria non associato ad alcun file usando la [**funzione AVIStreamCreate.**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) Questa funzione restituisce l'indirizzo dell'interfaccia al nuovo flusso in una posizione specificata e viene usata internamente da altre funzioni che creano flussi temporanei.

È possibile creare un flusso compresso da un flusso non compresso usando la [**funzione AVIMakeCompressedStream.**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) Si identificano il flusso da comprimere, il metodo di compressione e le opzioni di compressione e il gestore per il nuovo flusso.

Dopo aver terminato di usare un flusso creato con **AVIStreamCreate** o **AVIMakeCompressedStream,** chiudere il flusso usando la [**funzione AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) **AVIStreamRelease** libera le risorse usate dal flusso temporaneo.

 

 




