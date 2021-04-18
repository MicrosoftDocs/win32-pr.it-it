---
description: Un'applicazione che supporta i contatori delle prestazioni deve avere una chiave di prestazioni nella chiave dei servizi. Nell'esempio seguente vengono illustrati i valori che è necessario includere per questa chiave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Creazione della chiave delle prestazioni delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312177"
---
# <a name="creating-the-applications-performance-key"></a>Creazione della chiave delle prestazioni dell'applicazione

Un'applicazione che supporta i contatori delle prestazioni deve avere una chiave di **prestazioni** nella chiave **dei servizi** . Nell'esempio seguente vengono illustrati i valori che è necessario includere per questa chiave.

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

Il valore della **libreria** fornisce il nome della DLL di prestazioni e i valori di **apertura**, **raccolta** e **chiusura** forniscono i nomi delle funzioni esportate dalla DLL delle prestazioni. Il tipo di dati di questi valori è **reg \_ SZ**. Quando un consumer richiede dati sulle prestazioni, questi valori vengono utilizzati dal sistema per determinare quali DLL di prestazioni caricare e quali funzioni DLL chiamare.

Il valore della **raccolta** può contenere il nome della dll o il percorso completo della dll. Se si usa il tipo di dati **reg \_ expand \_ SZ** per la **libreria**, è possibile specificare le variabili di ambiente nel percorso.

La chiave del servizio dell'applicazione deve esistere prima di poter eseguire **lodctr** per caricare i nomi dei contatori e le stringhe della guida.

Per altri valori del registro di sistema che è possibile creare, ad esempio per specificare i valori di timeout per le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , vedere [creazione di altre voci del registro di sistema](creating-other-registry-entries.md).

 

 
