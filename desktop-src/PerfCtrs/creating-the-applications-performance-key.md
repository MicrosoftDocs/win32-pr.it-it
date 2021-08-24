---
description: Un'applicazione che supporta i contatori delle prestazioni deve avere una chiave prestazioni nella chiave Servizi. Nell'esempio seguente vengono illustrati i valori che è necessario includere per questa chiave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Creazione della chiave delle prestazioni delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149e8142b892edeb43f5459fe68bc6ad4b7453118c64cb2e288bb334c054fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144034"
---
# <a name="creating-the-applications-performance-key"></a>Creazione della chiave delle prestazioni dell'applicazione

Un'applicazione che supporta i contatori delle prestazioni deve avere una **chiave prestazioni** nella **chiave** Servizi. Nell'esempio seguente vengono illustrati i valori che è necessario includere per questa chiave.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

Il **valore Library** fornisce il nome della DLL delle prestazioni e i valori **Open**, **Collect** **e Close** forniscono i nomi delle funzioni esportate dalla DLL delle prestazioni. Il tipo di dati di questi valori è **REG \_ SZ**. Quando un consumer richiede dati sulle prestazioni, il sistema usa questi valori per determinare quali DLL delle prestazioni caricare e quali funzioni DLL chiamare.

Il **valore Library** può contenere il nome della DLL o un percorso completo della DLL. Se si usa il **tipo di dati REG EXPAND \_ \_ SZ** per **Library**, è possibile specificare variabili di ambiente nel percorso.

La chiave del servizio dell'applicazione deve esistere prima di poter eseguire **lodctr** per caricare i nomi dei contatori e le stringhe della Guida.

Per altri valori del Registro di sistema che è possibile creare, ad esempio per specificare valori di timeout per le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData,**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) vedere Creazione di altre voci del Registro [di sistema](creating-other-registry-entries.md).

 

 
