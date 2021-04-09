---
description: È possibile utilizzare le funzioni seguenti per lavorare con i dati sulle prestazioni in Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Funzioni dei contatori delle prestazioni per Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881746"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Funzioni dei contatori delle prestazioni per Visual Basic

> [!IMPORTANT]
> Le funzioni descritte in questo argomento possono essere modificate o non disponibili in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

È possibile utilizzare le funzioni seguenti per lavorare con i dati sulle prestazioni in Visual Basic.

- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhVbAddCounter**](pdhvbaddcounter.md)
- [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
- [**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
- [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
- [**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
- [**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
- [**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
- [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
- [**PdhVbOpenLog**](pdhvbopenlog.md)
- [**PdhVbOpenQuery**](pdhvbopenquery.md)
- [**PdhVbUpdateLog**](pdhvbupdatelog.md)

> [!NOTE]
> Le `PdhVb***` funzioni funzionano in una sessione per processo e non sono thread-safe. Queste funzioni devono essere usate solo da semplici applicazioni a thread singolo.
