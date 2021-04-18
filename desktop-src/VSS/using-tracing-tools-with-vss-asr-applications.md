---
description: È possibile utilizzare lo strumento logman per raccogliere informazioni di traccia per le applicazioni VSS che utilizzano il ripristino automatico del sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Uso degli strumenti di traccia con le applicazioni ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307183"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Uso degli strumenti di traccia con le applicazioni ASR

È possibile utilizzare lo strumento logman per raccogliere informazioni di traccia per le applicazioni VSS che utilizzano il [Ripristino automatico del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md). Logman (logman.exe) è un controller di traccia per gli eventi di traccia e i contatori delle prestazioni. È incluso in Windows XP e nelle versioni successive di Windows. In alternativa, se si preferisce, è possibile usare lo strumento tracelog per raccogliere le stesse informazioni di traccia di ASR. Tracelog è incluso in Windows Driver Kit (WDK).

Per usare gli strumenti di traccia con VSS, vedere [uso degli strumenti di traccia con VSS](using-tracing-tools-with-vss.md).

## <a name="using-logman"></a>Uso di logman

Nella procedura seguente viene descritto come utilizzare logman con l'applicazione ASR.

**Per usare logman con l'applicazione ASR**

1.  Usare il comando seguente per avviare la traccia:

    **logman avviare ASR-o** *x: \\ * * * ASR. etl-ETS-p {6407345b-94F2-44c8-b3db-4e076be46816} 0xFF 0xFF**

    > [!Note]  
    > Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia. Per prestazioni ottimali, il file di log di traccia deve trovarsi in un volume che non fa parte della copia shadow.

     

2.  Usare il comando seguente per arrestare la traccia:

    **logman stop ASR-ETS**

Il file di log di traccia è *x: \\* ASR. etl.

Per ulteriori informazioni sullo strumento Logman, vedere [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Uso di tracelog

Nella procedura seguente viene descritto come utilizzare tracelog.

**Per usare tracelog**

1.  Creare un file di testo denominato ASR. CTL che contiene solo il testo seguente:

    **6407345b-94F2-44c8-b3db-4e076be46816 ASR**

2.  Usare il comando seguente per avviare la traccia:

    **tracelog-avviare ASR-f** *x: \\ * * * ASR. etl-GUID ASR. CTL-flag 0xFF-Level 0xFF**

    > [!Note]  
    > Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia. Per prestazioni ottimali, il file di log di traccia deve trovarsi in un volume che non fa parte della copia shadow.

     

3.  Usare il comando seguente per arrestare la traccia:

    **tracelog-arresta ASR**

Il file di log di traccia è *x: \\* ASR. etl.

Per ulteriori informazioni sullo strumento tracelog, vedere [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
