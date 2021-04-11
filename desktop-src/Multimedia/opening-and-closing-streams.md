---
title: Apertura e chiusura di flussi
description: Apertura e chiusura di flussi
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream (funzione)
- AVIStreamRelease (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044430"
---
# <a name="opening-and-closing-streams"></a>Apertura e chiusura di flussi

L'apertura di flussi di dati è simile all'apertura di file. È possibile aprire un flusso usando la funzione [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) . Questa funzione crea un'interfaccia di flusso, inserisce un handle del flusso nell'interfaccia e restituisce un puntatore all'interfaccia. **AVIFileGetStream** gestisce anche un conteggio dei riferimenti delle applicazioni che hanno aperto un flusso, ma non quelle che lo hanno chiuso.

Se si vuole accedere a un singolo flusso in un file, è possibile aprire il file e il flusso usando la funzione [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) . Questa funzione combina le operazioni e gli argomenti della funzione delle funzioni [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileGetStream** .

Per accedere a più di un flusso in un file, usare **AVIFileOpen** una volta seguito da più chiamate a **AVIFileGetStream**.

È possibile incrementare il conteggio dei riferimenti di un flusso usando la funzione [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) per lasciare aperto un flusso quando si usa una funzione che in genere chiude il flusso.

È possibile chiudere un flusso usando la funzione [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Questa funzione decrementa il conteggio dei riferimenti del flusso e lo chiude quando il conteggio dei riferimenti raggiunge zero. Le applicazioni devono bilanciare il conteggio dei riferimenti includendo una chiamata a **AVIStreamRelease** per ogni uso della funzione [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** o **AVIStreamOpenFromFile** . Quando si rilascia un flusso aperto tramite **AVIStreamOpenFromFile**, avifile chiude il file contenente il flusso. Se l'applicazione rilascia un file con flussi di dati aperti, AVIFile non chiuderà i flussi finché non verranno rilasciati tutti i flussi.

 

 




