---
title: Apertura e chiusura di Flussi
description: Apertura e chiusura di Flussi
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- Funzione AVIFileGetStream
- Funzione AVIStreamRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35f678f2858d590956bc3ba724abacd12d2047e337fc8428934e0e32005bb24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038311"
---
# <a name="opening-and-closing-streams"></a>Apertura e chiusura di Flussi

L'apertura dei flussi di dati è simile all'apertura di file. È possibile aprire un flusso usando la [**funzione AVIFileGetStream.**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) Questa funzione crea un'interfaccia di flusso, inserisce un handle del flusso nell'interfaccia e restituisce un puntatore all'interfaccia. **AVIFileGetStream** gestisce anche un conteggio dei riferimenti delle applicazioni che hanno aperto un flusso, ma non di quelle che lo hanno chiuso.

Se si vuole accedere a un singolo flusso in un file, è possibile aprire il file e il flusso usando la [**funzione AVIStreamOpenFromFile.**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) Questa funzione combina le operazioni e gli argomenti delle funzioni [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) **e AVIFileGetStream.**

Per accedere a più flussi in un file, usare **AVIFileOpen** una volta seguito da più chiamate **ad AVIFileGetStream.**

È possibile incrementare il conteggio dei riferimenti di un flusso usando la funzione [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) per mantenere aperto un flusso quando si usa una funzione che normalmente chiude il flusso.

È possibile chiudere un flusso usando la [**funzione AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) Questa funzione decrementa il conteggio dei riferimenti del flusso e lo chiude quando il conteggio dei riferimenti raggiunge lo zero. Le applicazioni devono bilanciare il conteggio dei riferimenti includendo una chiamata ad **AVIStreamRelease** per ogni uso della funzione [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** o **AVIStreamOpenFromFile.** Quando si rilascia un flusso aperto tramite **AVIStreamOpenFromFile**, AVIFile chiude il file contenente il flusso. Se l'applicazione rilascia un file con flussi di dati aperti, AVIFile non chiuderà i flussi fino a quando non vengono rilasciati tutti i flussi.

 

 




