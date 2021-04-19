---
description: Quando si scrive un provider a prestazioni elevate che deriva classi da Win32 \_ PerfFormattedData, è necessario seguire convenzioni specifiche, in modo che WMI possa calcolare i valori delle proprietà.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Supporto della classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317546"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="fc773-103">Supporto della \_ classe Win32 PerfFormattedData</span><span class="sxs-lookup"><span data-stu-id="fc773-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="fc773-104">Quando si scrive un provider a prestazioni elevate che deriva classi da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), è necessario seguire convenzioni specifiche, in modo che WMI possa calcolare i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc773-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="fc773-105">La scrittura di un provider WMI a prestazioni elevate per la creazione di contatori delle prestazioni non è consigliata in alcuna versione del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="fc773-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="fc773-106">Per ulteriori informazioni, vedere la pagina relativa alla creazione di un [provider di istanze in un provider High-Performance e in](making-an-instance-provider-into-a-high-performance-provider.md)librerie di [prestazioni e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fc773-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="fc773-107">Nella procedura riportata di seguito viene descritto come supportare la \_ classe Win32 PerfFormattedData.</span><span class="sxs-lookup"><span data-stu-id="fc773-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="fc773-108">**Per supportare la \_ classe Win32 PerfFormattedData**</span><span class="sxs-lookup"><span data-stu-id="fc773-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="fc773-109">Creare la classe nello stesso spazio dei nomi della classe RAW corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fc773-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="fc773-110">La classe deve essere derivata da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e il qualificatore **HiPerf** è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="fc773-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="fc773-111">Per ulteriori informazioni sulla creazione di una classe personalizzata per WMI, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="fc773-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="fc773-112">Specificare "HiPerfCooker \_ V1" nel qualificatore del [**provider**](class-qualifiers-for-performance-counter-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="fc773-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="fc773-113">Specificare i qualificatori a livello di classe seguenti oltre ai qualificatori utilizzati per le classi non elaborate:</span><span class="sxs-lookup"><span data-stu-id="fc773-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="fc773-114">**Autocook**</span><span class="sxs-lookup"><span data-stu-id="fc773-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-115">**RawClass autocook \_**</span><span class="sxs-lookup"><span data-stu-id="fc773-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-116">**Cotto**</span><span class="sxs-lookup"><span data-stu-id="fc773-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-117">**Costose**</span><span class="sxs-lookup"><span data-stu-id="fc773-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-118">**Dinamico**</span><span class="sxs-lookup"><span data-stu-id="fc773-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="fc773-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="fc773-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-120">**Locale**</span><span class="sxs-lookup"><span data-stu-id="fc773-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-121">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="fc773-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-122">**Provider**</span><span class="sxs-lookup"><span data-stu-id="fc773-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-123">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="fc773-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="fc773-124">Non impostare alcun valore per **GenericPerfCtr**, **PerfIndex** o **HelpIndex** perché verranno impostati dal processo ADAP.</span><span class="sxs-lookup"><span data-stu-id="fc773-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="fc773-125">Per ulteriori informazioni, vedere [**qualificatori di classe per le classi dei contatori delle prestazioni**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="fc773-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="fc773-126">Includere una proprietà chiave denominata **Name** nella classe (questa proprietà non è obbligatoria per le classi singleton).</span><span class="sxs-lookup"><span data-stu-id="fc773-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="fc773-127">Il valore della proprietà **Name** deve essere uguale a quello della classe RAW corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fc773-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="fc773-128">Non è necessario usare alcuna proprietà chiave diversa da **Name** nella classe.</span><span class="sxs-lookup"><span data-stu-id="fc773-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="fc773-129">Creare i dati delle proprietà digitati come **DWORD** (**UInt32**) o **QWORD** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="fc773-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="fc773-130">Le proprietà devono corrispondere a una proprietà nella classe RAW o a una proprietà nella classe che si sta creando.</span><span class="sxs-lookup"><span data-stu-id="fc773-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="fc773-131">Specificare i seguenti qualificatori a livello di proprietà per tutte le proprietà della classe, oltre ai qualificatori **PerfIndex** e **PerfDetail** usati per le proprietà della classe RAW:</span><span class="sxs-lookup"><span data-stu-id="fc773-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="fc773-132">**Base**</span><span class="sxs-lookup"><span data-stu-id="fc773-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-133">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="fc773-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-134">**Contatore**</span><span class="sxs-lookup"><span data-stu-id="fc773-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-135">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="fc773-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-136">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="fc773-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="fc773-137">**SampleWindow**</span><span class="sxs-lookup"><span data-stu-id="fc773-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="fc773-138">Per ulteriori informazioni, vedere [**qualificatori di proprietà per le classi dei contatori delle prestazioni**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="fc773-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="fc773-139">Il file di intestazione Winperf. h contiene inoltre valori che è possibile specificare per **PerfDetail** e **CounterType**.</span><span class="sxs-lookup"><span data-stu-id="fc773-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="fc773-140">Verificare che il provider soddisfi i [requisiti di prestazioni](#performance-requirements).</span><span class="sxs-lookup"><span data-stu-id="fc773-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="fc773-141">Requisiti relativi alle prestazioni</span><span class="sxs-lookup"><span data-stu-id="fc773-141">Performance Requirements</span></span>

<span data-ttu-id="fc773-142">Quando si scrive un provider a prestazioni elevate, le prestazioni devono soddisfare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc773-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="fc773-143">L'apertura del file DLL a prestazioni elevate non può richiedere più di 100 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="fc773-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="fc773-144">In generale, l'apertura di ciascun provider a prestazioni elevate e la libreria delle prestazioni non può superare i 5 secondi.</span><span class="sxs-lookup"><span data-stu-id="fc773-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="fc773-145">L'aggiornamento dati non può richiedere più di 10 millisecondi per ogni raccolta.</span><span class="sxs-lookup"><span data-stu-id="fc773-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="fc773-146">In un'operazione di aggiornamento e raccolta complessiva tutti i provider a prestazioni elevate insieme non possono richiedere più di 800 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="fc773-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="fc773-147">Il carico complessivo della CPU per tutti i provider a prestazioni elevate non può superare il 6-7% di overhead della CPU o il 5% per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fc773-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc773-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc773-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc773-149">Creazione di un provider di istanze in un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="fc773-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
