---
description: Quando si scrive un provider a prestazioni elevate che deriva classi da Win32 \_ PerfRawData, è necessario seguire convenzioni specifiche, in modo che WMI possa fornire dati ai valori delle proprietà.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Supporto della classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309870"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="0c3d3-103">Supporto della \_ classe Win32 PerfRawData</span><span class="sxs-lookup"><span data-stu-id="0c3d3-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="0c3d3-104">Quando si scrive un provider a prestazioni elevate che deriva classi da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), è necessario seguire convenzioni specifiche, in modo che WMI possa fornire dati ai valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="0c3d3-105">La scrittura di un provider WMI a prestazioni elevate per la creazione di contatori delle prestazioni non è consigliata in alcuna versione del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="0c3d3-106">Per ulteriori informazioni, vedere la pagina relativa alla creazione di un [provider di istanze in un provider High-Performance e in](making-an-instance-provider-into-a-high-performance-provider.md)librerie di [prestazioni e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="0c3d3-107">Nella procedura riportata di seguito viene descritto come supportare la classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) con il provider a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="0c3d3-108">**Per supportare la \_ classe Win32 PerfRawData**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="0c3d3-109">Creare la classe nello \\ spazio dei nomi CIMv2 radice.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="0c3d3-110">La classe deve essere derivata da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e il qualificatore **HiPerf** è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="0c3d3-111">È inoltre possibile aggiungere classi di dati sulle prestazioni WDM (driver) allo \\ spazio dei nomi WMI radice.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="0c3d3-112">Per ulteriori informazioni sulla creazione di una classe personalizzata per WMI, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="0c3d3-113">Specificare il provider come "NT5 \_ GenericPerfProvider \_ V1" nel qualificatore del **provider** .</span><span class="sxs-lookup"><span data-stu-id="0c3d3-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="0c3d3-114">Specificare i qualificatori a livello di classe seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c3d3-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="0c3d3-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-115">**HiPerf**</span></span>
    -   <span data-ttu-id="0c3d3-116">**Impostazioni locali**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-116">**Locale**</span></span>
    -   <span data-ttu-id="0c3d3-117">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="0c3d3-118">**Provider**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-118">**Provider**</span></span>

    <span data-ttu-id="0c3d3-119">Per ulteriori informazioni, vedere [**qualificatori di classe per le classi dei contatori delle prestazioni**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="0c3d3-120">Non definire il qualificatore **GenericPerfCtr** perché è riservato per il processo ADAP che trasferisce i dati della libreria delle prestazioni in classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="0c3d3-121">Popola le proprietà timestamp e Frequency appropriate utilizzate per calcolare le formule di tipo contatore.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="0c3d3-122">Queste proprietà vengono ereditate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e, se si sta scrivendo un provider a prestazioni elevate, è necessario compilare tali proprietà affinché la classe venga visualizzata in Monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="0c3d3-123">Includere una proprietà chiave denominata **Name** nella classe (questa proprietà non è obbligatoria per le classi singleton).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="0c3d3-124">Non è necessario usare alcuna proprietà chiave diversa da **Name** nella classe.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="0c3d3-125">Crea proprietà dati tipizzati come **DWORD** (**UInt32**) o **QWORD** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="0c3d3-126">Queste proprietà diventano contatori delle prestazioni quando vengono trasferite alle librerie delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="0c3d3-127">Specificare i seguenti qualificatori a livello di proprietà per tutte le proprietà della classe:</span><span class="sxs-lookup"><span data-stu-id="0c3d3-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="0c3d3-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-128">**DisplayName**</span></span>
    -   <span data-ttu-id="0c3d3-129">**CounterType**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-129">**CounterType**</span></span>
    -   <span data-ttu-id="0c3d3-130">**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="0c3d3-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-131">**Description**</span></span>
    -   <span data-ttu-id="0c3d3-132">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="0c3d3-133">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="0c3d3-133">**PerfDetail**</span></span>

    <span data-ttu-id="0c3d3-134">Per ulteriori informazioni, vedere [**qualificatori di proprietà per le classi dei contatori delle prestazioni**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="0c3d3-135">Il file di intestazione Winperf. h contiene inoltre valori che è possibile specificare per **PerfDetail** e **CounterType**.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="0c3d3-136">WMI utilizza i qualificatori **DisplayName**, **locale** e **Description** per la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="0c3d3-137">È necessario aggiungere i qualificatori modificati allo \_ spazio dei nomi MS 409 (Inglese) in modo che monitor di sistema possa visualizzare correttamente i dati della classe.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="0c3d3-138">Ciò significa che è possibile modificare la definizione della proprietà aggiungendo un qualificatore di **Descrizione** con il testo esplicativo e compilare il valore **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="0c3d3-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="0c3d3-139">È inoltre necessario aggiungere qualificatori modificati a qualsiasi altro spazio dei nomi delle impostazioni locali supportato dalla classe.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="0c3d3-140">Se un utente richiede dati da impostazioni locali per le quali non si forniscono qualificatori corretti, WMI utilizza per impostazione predefinita le definizioni specificate nello \_ spazio dei nomi MS 409.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="0c3d3-141">Creare una proprietà di base per qualsiasi proprietà che dispone di un tipo di contatore che prevede un valore di base.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="0c3d3-142">Questa proprietà segue immediatamente la proprietà ed è denominata \* propertyName \***\_ base**.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="0c3d3-143">Ad esempio, la proprietà media **AvgDiskBytesPerRead** della classe [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) richiede una proprietà di base denominata **AvgDiskBytesPerRead \_ base** per contare il numero di campioni.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="0c3d3-144">Per determinare se il tipo di contatore che si desidera utilizzare richiede una proprietà di base, individuare il tipo di contatore in base al nome o al valore decimale nei [tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="0c3d3-145">Verificare che il provider soddisfi i [requisiti di prestazioni](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d3-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c3d3-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c3d3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c3d3-147">Creazione di un provider di istanze in un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="0c3d3-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
