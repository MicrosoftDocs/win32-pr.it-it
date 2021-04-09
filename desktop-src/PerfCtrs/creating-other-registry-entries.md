---
description: La funzione OpenPerformanceData delle DLL di prestazioni accetta un argomento di stringa come input.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Creazione di altre voci del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967519"
---
# <a name="creating-other-registry-entries"></a>Creazione di altre voci del registro di sistema

La funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) della DLL di prestazioni accetta un argomento di stringa come input. Per specificare una stringa di input per la funzione Open, includere una chiave di **collegamento** sotto la chiave **Services** . La chiave di **collegamento** contiene un valore di **esportazione** . Impostare i dati del valore da **esportare** sulla stringa di input che si desidera passare alla funzione Open. Il tipo di dati **Export** è **reg \_ \_ multisz**.

Se **Export** non è definito (**Export** è facoltativo), il sistema passa **null** alla funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .

In genere, se più di un'applicazione condivide la stessa DLL di prestazioni, ogni applicazione include una chiave di **collegamento** e un valore di **esportazione** per fornire il contesto in cui l'applicazione chiama la dll.

Di seguito vengono illustrate le voci del registro di sistema:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

Per impostazione predefinita, le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) della DLL di prestazioni devono restituire entro 10.000 millisecondi. In caso contrario, il sistema non utilizzerà i dati restituiti dalla DLL. L'applicazione può aumentare o diminuire il valore di timeout specificando un valore **Open Timeout** o **Collect Timeout** del registro di sistema sotto la relativa chiave **performance** come illustrato nell'esempio seguente.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

Per ottenere i dati sulle prestazioni per alcune applicazioni, ovvero quelle che restituiscono contatori mediante la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) , è necessario utilizzare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il dispositivo associato all'applicazione. In questo caso, il nome specificato in **CreateFile** deve essere installato anche nel nodo dispositivi DOS del registro di sistema, come illustrato di seguito:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
