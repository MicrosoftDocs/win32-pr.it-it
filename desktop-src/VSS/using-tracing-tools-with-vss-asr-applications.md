---
description: È possibile usare lo strumento Logman per raccogliere informazioni di traccia per le applicazioni VSS che usano Automated Ripristino di sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Uso degli strumenti di traccia con le applicazioni asr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2d22dbb1488b5fd60836926d3c5ef2de5913ff1cc1529fdb278773b2ccd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590870"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Uso degli strumenti di traccia con le applicazioni asr

È possibile usare lo strumento Logman per raccogliere informazioni di traccia per le applicazioni VSS che usano [Automated Ripristino di sistema (ASR).](using-vss-automated-system-recovery-for-disaster-recovery.md) Logman (logman.exe) è un controller di traccia per gli eventi di traccia e i contatori delle prestazioni. È incluso in Windows XP e versioni successive di Windows. Oppure, se si preferisce, è possibile usare lo strumento Tracelog per raccogliere le stesse informazioni di traccia asr. Tracelog è incluso in Windows Driver Kit (WDK).

Per usare gli strumenti di traccia con VSS, vedere [Uso degli strumenti di traccia con VSS.](using-tracing-tools-with-vss.md)

## <a name="using-logman"></a>Uso di Logman

La procedura seguente descrive come usare Logman con l'applicazione asr.

**Per usare Logman con l'applicazione asr**

1.  Usare il comando seguente per avviare la traccia:

    **logman start asr -o** *x: \\ ***asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff**

    > [!Note]  
    > Sostituire "x: " con il percorso della directory in cui si vuole archiviare il file di \\ log di traccia. Per prestazioni ottimali, il file di log di traccia deve trovarsi in un volume che non fa parte della copia shadow.

     

2.  Usare il comando seguente per arrestare la traccia:

    **logman stop asr -ets**

Il file di log di traccia *è x: \\* asr.etl.

Per altre informazioni sullo strumento Logman, vedere [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Uso del log di traccia

La procedura seguente descrive come usare Tracelog.

**Per usare Tracelog**

1.  Creare un file di testo denominato asr.ctl contenente solo il testo seguente:

    **6407345b-94f2-44c8-b3db-4e076be46816 asr**

2.  Usare il comando seguente per avviare la traccia:

    **tracelog -start asr -f** *x: \\ ***asr.etl -guid asr.ctl -flag 0xff -level 0xff**

    > [!Note]  
    > Sostituire "x: " con il percorso della directory in cui si vuole archiviare il file di \\ log di traccia. Per prestazioni ottimali, il file di log di traccia deve trovarsi in un volume che non fa parte della copia shadow.

     

3.  Usare il comando seguente per arrestare la traccia:

    **tracelog -stop asr**

Il file di log di traccia *è x: \\* asr.etl.

Per altre informazioni sullo strumento Tracelog, vedere [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
