---
description: Il Windows SDK (WSDK) contiene tre DLL di prestazioni di esempio complete.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Esempi di DLL di prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312102"
---
# <a name="performance-dll-samples"></a>Esempi di DLL di prestazioni

Il Windows SDK (WSDK) contiene tre DLL di prestazioni di esempio complete. Questi esempi si trovano nella directory Samples \\ winbase \\ WinNT \\ PerfTool \\ PerfDlls La radice di questo percorso è la directory di installazione di base di WSDK. È possibile scaricare WSDK dal [Software Development Kit (SDK) di Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (cercare Windows SDK e selezionare il download per l'ultimo sistema operativo rilasciato).

Gli esempi contenuti in questa directory sono:

-   **AppMem**: fornisce le controparti delle funzioni [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)e [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) che segnalano le informazioni sulle prestazioni. I contatori delle prestazioni nel registro di sistema e lo strumento prestazioni possono leggere le informazioni sulle prestazioni.
-   **LeakyBin**: illustra l'uso dei contatori delle prestazioni dell'applicazione.
-   **PerfGen**: offre tre forme d'onda a cinque periodi diversi per l'uso con lo strumento prestazioni per fornire dati con una velocità e un valore noti. Questa operazione può essere utile per il test di applicazioni che utilizzano dati sulle prestazioni e richiedono valori stimabili per i test.

 

 
