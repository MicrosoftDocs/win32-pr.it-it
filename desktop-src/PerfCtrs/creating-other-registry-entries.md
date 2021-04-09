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
# <a name="creating-other-registry-entries"></a><span data-ttu-id="1a768-103">Creazione di altre voci del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1a768-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="1a768-104">La funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) della DLL di prestazioni accetta un argomento di stringa come input.</span><span class="sxs-lookup"><span data-stu-id="1a768-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="1a768-105">Per specificare una stringa di input per la funzione Open, includere una chiave di **collegamento** sotto la chiave **Services** .</span><span class="sxs-lookup"><span data-stu-id="1a768-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="1a768-106">La chiave di **collegamento** contiene un valore di **esportazione** .</span><span class="sxs-lookup"><span data-stu-id="1a768-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="1a768-107">Impostare i dati del valore da **esportare** sulla stringa di input che si desidera passare alla funzione Open.</span><span class="sxs-lookup"><span data-stu-id="1a768-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="1a768-108">Il tipo di dati **Export** è **reg \_ \_ multisz**.</span><span class="sxs-lookup"><span data-stu-id="1a768-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="1a768-109">Se **Export** non è definito (**Export** è facoltativo), il sistema passa **null** alla funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1a768-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="1a768-110">In genere, se più di un'applicazione condivide la stessa DLL di prestazioni, ogni applicazione include una chiave di **collegamento** e un valore di **esportazione** per fornire il contesto in cui l'applicazione chiama la dll.</span><span class="sxs-lookup"><span data-stu-id="1a768-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="1a768-111">Di seguito vengono illustrate le voci del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="1a768-111">The following shows the registry entries:</span></span>

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

<span data-ttu-id="1a768-112">Per impostazione predefinita, le funzioni [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) della DLL di prestazioni devono restituire entro 10.000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="1a768-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="1a768-113">In caso contrario, il sistema non utilizzerà i dati restituiti dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="1a768-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="1a768-114">L'applicazione può aumentare o diminuire il valore di timeout specificando un valore **Open Timeout** o **Collect Timeout** del registro di sistema sotto la relativa chiave **performance** come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="1a768-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

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

<span data-ttu-id="1a768-115">Per ottenere i dati sulle prestazioni per alcune applicazioni, ovvero quelle che restituiscono contatori mediante la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) , è necessario utilizzare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il dispositivo associato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a768-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="1a768-116">In questo caso, il nome specificato in **CreateFile** deve essere installato anche nel nodo dispositivi DOS del registro di sistema, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="1a768-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
