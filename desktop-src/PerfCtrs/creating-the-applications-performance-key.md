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
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="32640-104">Creazione della chiave delle prestazioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="32640-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="32640-105">Un'applicazione che supporta i contatori delle prestazioni deve avere una chiave di **prestazioni** nella chiave **dei servizi** .</span><span class="sxs-lookup"><span data-stu-id="32640-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="32640-106">Nell'esempio seguente vengono illustrati i valori che è necessario includere per questa chiave.</span><span class="sxs-lookup"><span data-stu-id="32640-106">The following example shows the values that you must include for this key.</span></span>

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

<span data-ttu-id="32640-107">Il valore della **libreria** fornisce il nome della DLL di prestazioni e i valori di **apertura**, **raccolta** e **chiusura** forniscono i nomi delle funzioni esportate dalla DLL delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="32640-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="32640-108">Il tipo di dati di questi valori è **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="32640-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="32640-109">Quando un consumer richiede dati sulle prestazioni, questi valori vengono utilizzati dal sistema per determinare quali DLL di prestazioni caricare e quali funzioni DLL chiamare.</span><span class="sxs-lookup"><span data-stu-id="32640-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="32640-110">Il valore della **raccolta** può contenere il nome della dll o il percorso completo della dll.</span><span class="sxs-lookup"><span data-stu-id="32640-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="32640-111">Se si usa il tipo di dati **reg \_ expand \_ SZ** per la **libreria**, è possibile specificare le variabili di ambiente nel percorso.</span><span class="sxs-lookup"><span data-stu-id="32640-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="32640-112">La chiave del servizio dell'applicazione deve esistere prima di poter eseguire **lodctr** per caricare i nomi dei contatori e le stringhe della guida.</span><span class="sxs-lookup"><span data-stu-id="32640-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="32640-113">Per altri valori del registro di sistema che è possibile creare, ad esempio per specificare i valori di timeout per le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , vedere [creazione di altre voci del registro di sistema](creating-other-registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="32640-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
