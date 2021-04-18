---
description: Sebbene esistano pochi limiti tecnici per il tipo e le dimensioni dei dati che un'applicazione può archiviare nel registro di sistema, sono disponibili alcune linee guida pratiche per promuovere l'efficienza del sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Spazio di archiviazione del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313260"
---
# <a name="registry-storage-space"></a><span data-ttu-id="2ca10-103">Spazio di archiviazione del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2ca10-103">Registry Storage Space</span></span>

<span data-ttu-id="2ca10-104">Sebbene esistano pochi limiti tecnici per il tipo e le dimensioni dei dati che un'applicazione può archiviare nel registro di sistema, sono disponibili alcune linee guida pratiche per promuovere l'efficienza del sistema.</span><span class="sxs-lookup"><span data-stu-id="2ca10-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="2ca10-105">Un'applicazione deve archiviare i dati di configurazione e di inizializzazione nel registro di sistema e archiviare altri tipi di dati altrove.</span><span class="sxs-lookup"><span data-stu-id="2ca10-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="2ca10-106">In genere, i dati costituiti da più di uno o due kilobyte (K) devono essere archiviati come file e a cui viene fatto riferimento tramite una chiave nel registro di sistema anziché essere archiviati come valore.</span><span class="sxs-lookup"><span data-stu-id="2ca10-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="2ca10-107">Anziché duplicare grandi quantità di dati nel registro di sistema, un'applicazione deve salvare i dati come file e fare riferimento al file.</span><span class="sxs-lookup"><span data-stu-id="2ca10-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="2ca10-108">Il codice binario eseguibile non deve mai essere archiviato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ca10-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="2ca10-109">Una voce di valore usa molto meno spazio del registro di sistema rispetto a una chiave.</span><span class="sxs-lookup"><span data-stu-id="2ca10-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="2ca10-110">Per risparmiare spazio, un'applicazione deve raggruppare dati simili come una struttura e archiviare la struttura come valore anziché archiviare ogni membro della struttura come chiave separata.</span><span class="sxs-lookup"><span data-stu-id="2ca10-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="2ca10-111">L'archiviazione dei dati in formato binario consente a un'applicazione di archiviare i dati in un valore che altrimenti sarebbe costituito da diversi tipi incompatibili.</span><span class="sxs-lookup"><span data-stu-id="2ca10-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="2ca10-112">Viene eseguito il mapping delle visualizzazioni dei file del registro di sistema nella memoria del pool di paging.</span><span class="sxs-lookup"><span data-stu-id="2ca10-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="2ca10-113">**Windows server 2008 per 32 bit, Windows Vista con SP1 per 32 bit, Windows Vista, Windows server 2003, Windows XP:** Le visualizzazioni dei file del registro di sistema vengono mappate nello spazio degli indirizzi della cache del computer.</span><span class="sxs-lookup"><span data-stu-id="2ca10-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="2ca10-114">Di conseguenza, indipendentemente dalle dimensioni dei dati del registro di sistema, non viene addebitato più di 4 megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="2ca10-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="2ca10-115">La dimensione massima di un hive del registro di sistema è di 2 GB, ad eccezione dell'hive di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ca10-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="2ca10-116">**Windows server 2003 con SP1, Windows server 2003 e Windows XP:** Non sono previsti limiti espliciti sulla quantità totale di spazio che può essere utilizzata dagli hive nella memoria del pool di paging e nello spazio su disco, anche se le quote di sistema possono influire sulle dimensioni massime effettive.</span><span class="sxs-lookup"><span data-stu-id="2ca10-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="2ca10-117">Le dimensioni massime di un hive del registro di sistema sono limitate a 2 GB a partire da Windows Server 2003 con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="2ca10-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="2ca10-118">La dimensione massima dell'hive di sistema è limitata dalla memoria fisica, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2ca10-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="2ca10-119">Sistema</span><span class="sxs-lookup"><span data-stu-id="2ca10-119">System</span></span>                      | <span data-ttu-id="2ca10-120">Dimensioni massime dell'hive di sistema</span><span class="sxs-lookup"><span data-stu-id="2ca10-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca10-121">sistemi basati su x86</span><span class="sxs-lookup"><span data-stu-id="2ca10-121">x86-based systems</span></span>           | <span data-ttu-id="2ca10-122">50% della memoria fisica, fino a 400 MB. **Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 e Windows XP:** 25% della memoria fisica, fino a 200 MB.</span><span class="sxs-lookup"><span data-stu-id="2ca10-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="2ca10-123">sistemi basati su x64</span><span class="sxs-lookup"><span data-stu-id="2ca10-123">x64-based systems</span></span>           | <span data-ttu-id="2ca10-124">50% della memoria fisica, fino a 1,5 GB. **Windows Server 2003 con SP2:** 25% della memoria di sistema, fino a 200 MB.</span><span class="sxs-lookup"><span data-stu-id="2ca10-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="2ca10-125">**Windows server 2003 con SP1, Windows server 2003 e Windows XP 64-bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="2ca10-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="2ca10-126">Sistemi basati su Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="2ca10-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="2ca10-127">50% della memoria fisica, fino a 1 GB. **Windows server 2008, Windows Vista, Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 e Windows XP 64-bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="2ca10-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="2ca10-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2ca10-128">Windows 2000</span></span>

<span data-ttu-id="2ca10-129">I dati del registro di sistema vengono archiviati nel pool di paging, un'area di memoria fisica usata per i dati di sistema che possono essere scritti su disco quando non sono in uso.</span><span class="sxs-lookup"><span data-stu-id="2ca10-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="2ca10-130">Il valore **RegistrySizeLimit** stabilisce la quantità massima di pool di paging che può essere utilizzata dai dati del registro di sistema di tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca10-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="2ca10-131">Questo valore si trova nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="2ca10-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="2ca10-132">Per impostazione predefinita, il limite di dimensioni del registro di sistema è pari al 25% del pool di paging.</span><span class="sxs-lookup"><span data-stu-id="2ca10-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="2ca10-133">(La dimensione predefinita del pool di paging è 32 MB, quindi è 8 MB). Il sistema garantisce che il valore minimo di **RegistrySizeLimit** sia 4 MB e il valore massimo sia pari a circa il 80% del valore di **PagedPoolSize** .</span><span class="sxs-lookup"><span data-stu-id="2ca10-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="2ca10-134">Se il valore di questa voce è maggiore del 80% delle dimensioni del pool di paging, il sistema imposta le dimensioni massime del registro di sistema sul 80% delle dimensioni del pool di paging.</span><span class="sxs-lookup"><span data-stu-id="2ca10-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="2ca10-135">In questo modo si impedisce al registro di sistema di usare lo spazio necessario per i processi.</span><span class="sxs-lookup"><span data-stu-id="2ca10-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="2ca10-136">Si noti che l'impostazione di questo valore non consente di allocare spazio nel pool di paging, né garantisce che lo spazio sarà disponibile se necessario.</span><span class="sxs-lookup"><span data-stu-id="2ca10-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="2ca10-137">Le dimensioni del pool di paging sono determinate dal valore **PagedPoolSize** nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="2ca10-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="2ca10-138">Per un esempio di come determinare le dimensioni correnti e massime del registro di sistema, vedere [determinazione delle dimensioni del registro](determining-the-registry-size.md)di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ca10-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="2ca10-139">Il pool di paging massimo è di circa 300.470 MB, pertanto il limite delle dimensioni del registro di sistema è 240-376 MB.</span><span class="sxs-lookup"><span data-stu-id="2ca10-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="2ca10-140">Tuttavia, se si usa l'opzione/3GB, le dimensioni massime del pool di paging sono pari a 192 MB, quindi il registro di sistema può avere un massimo di 153,6 MB.</span><span class="sxs-lookup"><span data-stu-id="2ca10-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 




