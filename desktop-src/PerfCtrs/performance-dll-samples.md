---
description: In Windows SDK (WSDK) sono contenute tre DLL complete per le prestazioni di esempio.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Esempi di DLL per le prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94e77ed35b1c328879ad5f83dded45fe92bf4a62ae15c794e5d9d9b23daeda1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143884"
---
# <a name="performance-dll-samples"></a>Esempi di DLL per le prestazioni

In Windows SDK (WSDK) sono contenute tre DLL complete per le prestazioni di esempio. Questi esempi si trovano nella directory Samples \\ WinBase \\ WinNT \\ \\ PerfTool PerfDlls. La radice di questo percorso è la directory di installazione di base di WSDK. È possibile scaricare WSDK da [Microsoft Windows Software Development Kit (SDK) (cercare](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) Windows SDK e selezionare il download per il sistema operativo più recente rilasciato).

Gli esempi contenuti in questa directory sono:

-   **AppMem:** fornisce le controparti delle [**funzioni GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)e [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) che forniscono informazioni sulle prestazioni. I contatori delle prestazioni nel Registro di sistema e nello strumento Prestazioni possono leggere le informazioni sulle prestazioni.
-   **LeakyBin:** illustra l'uso dei contatori delle prestazioni dell'applicazione.
-   **PerfGen:** fornisce tre forme d'onda in cinque periodi diversi da usare con lo strumento Prestazioni per fornire dati a una velocità e a un valore noti. Ciò può essere utile per testare le applicazioni che usano dati sulle prestazioni e che necessitano di valori stimabili rispetto a cui eseguire il test.

 

 
