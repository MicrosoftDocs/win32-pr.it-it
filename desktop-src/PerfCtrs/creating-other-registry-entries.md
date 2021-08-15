---
description: La funzione OpenPerformanceData delle DLL delle prestazioni accetta un argomento stringa come input.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Creazione di altre voci del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ad9fe960713a481ba5a9b8f4b73e11bdbdd4d9fe9474b04b994e373ce8e1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683971"
---
# <a name="creating-other-registry-entries"></a>Creazione di altre voci del Registro di sistema

La funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) della DLL delle prestazioni accetta un argomento stringa come input. Per fornire una stringa di input alla funzione aperta, includere una **chiave di collegamento** sotto la chiave **Services.** La **chiave Linkage** contiene un **valore export.** Impostare i dati del valore **per Esporta** sulla stringa di input che si vuole passare alla funzione aperta. Il tipo di dati **di Export** è REG **MULTI \_ \_ SZ.**

Se **Export** non è definito (**Export** è facoltativo), il sistema passa **NULL** alla [**funzione OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

In genere, se più applicazioni condividono la stessa  DLL delle  prestazioni, ogni applicazione include una chiave di collegamento e un valore di esportazione per fornire il contesto in cui l'applicazione chiama la DLL.

Di seguito sono illustrate le voci del Registro di sistema:

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

Per impostazione predefinita, le funzioni [**OpenPerformanceData e CollectPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) della DLL delle prestazioni devono restituire entro 10.000 millisecondi. [](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) In caso contrario, il sistema non utilizza i dati restituiti dalla DLL. L'applicazione può aumentare o diminuire il valore di timeout specificando un valore del Registro di sistema **Open Timeout** o **Collect Timeout** sotto la relativa chiave **Performance,** come illustrato nell'esempio seguente.

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

Per ottenere i dati sulle prestazioni per alcune applicazioni(quelli che restituiscono contatori usando la funzione [**DeviceIoControl),**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) è necessario usare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il dispositivo associato all'applicazione. In questo caso, il nome specificato in **CreateFile** deve essere installato anche nel nodo Dispositivi DOS del Registro di sistema, come illustrato di seguito:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
