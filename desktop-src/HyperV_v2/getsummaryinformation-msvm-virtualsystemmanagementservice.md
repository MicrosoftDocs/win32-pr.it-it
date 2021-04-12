---
description: Restituisce informazioni di riepilogo sulla macchina virtuale.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Metodo GetSummaryInformation della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342801"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ad827-103">Metodo GetSummaryInformation della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ad827-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ad827-104">Restituisce informazioni di riepilogo sulla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad827-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad827-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad827-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="ad827-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad827-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad827-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad827-108">Tipo: **CIM \_ VirtualSystemSettingData \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ad827-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="ad827-109">Matrice di istanze [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che specificano le macchine virtuali o gli snapshot per cui è necessario recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="ad827-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="ad827-110">Se questo parametro è **null**, vengono recuperate le informazioni per tutte le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ad827-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="ad827-111">*RequestedInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad827-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad827-112">Tipo: **UInt32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ad827-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="ad827-113">Matrice di valori di enumerazione, che corrisponde alle proprietà della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , che specificano i dati da recuperare per le macchine virtuali e gli snapshot specificati nella matrice *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="ad827-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="ad827-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome** (0)</span><span class="sxs-lookup"><span data-stu-id="ad827-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-115">Corrisponde alla proprietà **Name** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="ad827-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nome elemento** (1)</span><span class="sxs-lookup"><span data-stu-id="ad827-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-117">Corrisponde alla proprietà **ElementName** della classe SummaryInformation di [**MSVM \_**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="ad827-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Ora creazione** (2)</span><span class="sxs-lookup"><span data-stu-id="ad827-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-119">Corrisponde alla proprietà **creationTime** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="ad827-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Note** (3)</span><span class="sxs-lookup"><span data-stu-id="ad827-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-121">Corrisponde alla proprietà **Notes** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="ad827-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Numero di processori** (4)</span><span class="sxs-lookup"><span data-stu-id="ad827-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-123">Corrisponde alla proprietà **NumberOfProcessors** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="ad827-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Piccola immagine di anteprima (80x60)** (5)</span><span class="sxs-lookup"><span data-stu-id="ad827-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-125">Corrisponde alla proprietà **ThumbnailImage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="ad827-126">Verrà recuperata un'immagine di anteprima con dimensioni pari a 80 60.</span><span class="sxs-lookup"><span data-stu-id="ad827-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="ad827-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Immagine di anteprima media (160x120)** (6)</span><span class="sxs-lookup"><span data-stu-id="ad827-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-128">Corrisponde alla proprietà **ThumbnailImage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="ad827-129">Verrà recuperata un'immagine di anteprima con dimensioni pari a 160 120.</span><span class="sxs-lookup"><span data-stu-id="ad827-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="ad827-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Immagine di anteprima grande (320x240)** (7)</span><span class="sxs-lookup"><span data-stu-id="ad827-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-131">Corrisponde alla proprietà **ThumbnailImage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="ad827-132">Verrà recuperata un'immagine di anteprima con dimensioni pari a 320 240.</span><span class="sxs-lookup"><span data-stu-id="ad827-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="ad827-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span><span class="sxs-lookup"><span data-stu-id="ad827-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-134">Corrisponde alla proprietà **AllocatedGPU** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="ad827-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span><span class="sxs-lookup"><span data-stu-id="ad827-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="ad827-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione** (10)</span><span class="sxs-lookup"><span data-stu-id="ad827-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="ad827-137">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ad827-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="ad827-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Schermato** (11)</span><span class="sxs-lookup"><span data-stu-id="ad827-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="ad827-139">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ad827-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="ad827-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span><span class="sxs-lookup"><span data-stu-id="ad827-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-141">Corrisponde alla proprietà **EnabledState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="ad827-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span><span class="sxs-lookup"><span data-stu-id="ad827-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-143">Corrisponde alla proprietà **ProcessorLoad** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="ad827-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span><span class="sxs-lookup"><span data-stu-id="ad827-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-145">Corrisponde alla proprietà **ProcessorLoadHistory** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="ad827-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span><span class="sxs-lookup"><span data-stu-id="ad827-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-147">Corrisponde alla proprietà **MemoryUsage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="ad827-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span><span class="sxs-lookup"><span data-stu-id="ad827-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-149">Corrisponde alla proprietà **heartbeat** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="ad827-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tempo di esecuzione** (105)</span><span class="sxs-lookup"><span data-stu-id="ad827-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-151">Corrisponde alla proprietà di **tempo di esecuzione** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="ad827-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span><span class="sxs-lookup"><span data-stu-id="ad827-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-153">Corrisponde alla proprietà **GuestOperatingSystem** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="ad827-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshot** (107)</span><span class="sxs-lookup"><span data-stu-id="ad827-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-155">Corrisponde alla proprietà **Snapshots** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="ad827-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span><span class="sxs-lookup"><span data-stu-id="ad827-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-157">Corrisponde alla proprietà **AsynchronousTasks** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="ad827-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span><span class="sxs-lookup"><span data-stu-id="ad827-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-159">Corrisponde alla proprietà **HealthState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="ad827-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span><span class="sxs-lookup"><span data-stu-id="ad827-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-161">Corrisponde alla proprietà **OperationalStatus** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="ad827-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span><span class="sxs-lookup"><span data-stu-id="ad827-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-163">Corrisponde alla proprietà **StatusDescriptions** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="ad827-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span><span class="sxs-lookup"><span data-stu-id="ad827-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-165">Corrisponde alla proprietà **MemoryAvailable** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="ad827-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span><span class="sxs-lookup"><span data-stu-id="ad827-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-167">Corrisponde alla proprietà **AvailableMemoryBuffer** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="ad827-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modalità di replica** (114)</span><span class="sxs-lookup"><span data-stu-id="ad827-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-169">Corrisponde alla proprietà **ReplicationMode** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="ad827-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Stato di replica** (115)</span><span class="sxs-lookup"><span data-stu-id="ad827-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-171">Corrisponde alla proprietà **ReplicationState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="ad827-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Sistema di replica HealthTest di replica** (116)</span><span class="sxs-lookup"><span data-stu-id="ad827-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-173">Corrisponde alla proprietà **ReplicationHealth** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="ad827-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Integrità dell'applicazione** (117)</span><span class="sxs-lookup"><span data-stu-id="ad827-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="ad827-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span><span class="sxs-lookup"><span data-stu-id="ad827-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-176">Corrisponde alla proprietà **ReplicationState** della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="ad827-177">Si tratta di una matrice per tutti i valori dello stato di replica tra relazioni primarie ed estese.</span><span class="sxs-lookup"><span data-stu-id="ad827-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="ad827-178">il valore di indice 0 è sempre per la relazione primaria e, se la replica estesa è abilitata, viene restituita nell'indice 1.</span><span class="sxs-lookup"><span data-stu-id="ad827-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="ad827-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span><span class="sxs-lookup"><span data-stu-id="ad827-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-180">Corrisponde alla proprietà **ReplicationHealth** della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="ad827-181">Si tratta di una matrice per tutti i valori di integrità della replica tra relazioni primarie ed estese.</span><span class="sxs-lookup"><span data-stu-id="ad827-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="ad827-182">il valore di indice 0 è sempre per la relazione primaria e, se la replica estesa è abilitata, viene restituita nell'indice 1.</span><span class="sxs-lookup"><span data-stu-id="ad827-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="ad827-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span><span class="sxs-lookup"><span data-stu-id="ad827-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-184">Corrisponde alla proprietà **SwapFilesInUse** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="ad827-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span><span class="sxs-lookup"><span data-stu-id="ad827-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="ad827-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span><span class="sxs-lookup"><span data-stu-id="ad827-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-187">Corrisponde alla proprietà **Name** della classe [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="ad827-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span><span class="sxs-lookup"><span data-stu-id="ad827-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="ad827-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span><span class="sxs-lookup"><span data-stu-id="ad827-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-190">Corrisponde alla proprietà **IntegrationServicesVersionState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="ad827-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span><span class="sxs-lookup"><span data-stu-id="ad827-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="ad827-192">Corrisponde alla proprietà **OtherEnabledState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad827-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="ad827-193">(133)</span><span class="sxs-lookup"><span data-stu-id="ad827-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ad827-194">*SummaryInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad827-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad827-195">Tipo: **[ **MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="ad827-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="ad827-196">Matrice di istanze di [**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md) contenenti le informazioni richieste per le macchine virtuali e/o gli snapshot specificati nella matrice *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="ad827-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="ad827-197">Questa matrice avrà lo stesso numero di elementi della matrice *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="ad827-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="ad827-198">Ognuna di queste voci conterrà la proprietà **Name** , anche se questa proprietà non è stata richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad827-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="ad827-199">Se la macchina virtuale o lo snapshot non è stato trovato o non è disponibile, la proprietà **Name** della voce di informazioni di riepilogo corrispondente sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="ad827-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="ad827-200">Le proprietà non specificate nel parametro *RequestedInformation* avranno un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="ad827-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="ad827-201">DataType aggiornato da in Windows 10, versione 1703 da [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="ad827-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad827-202">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad827-202">Return value</span></span>

<span data-ttu-id="ad827-203">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad827-203">Type: **uint32**</span></span>

<span data-ttu-id="ad827-204">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad827-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ad827-205">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ad827-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-206">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ad827-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-207">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="ad827-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-208">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="ad827-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-209">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="ad827-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-210">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="ad827-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-211">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ad827-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-212">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ad827-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-213">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ad827-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-214">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="ad827-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-215">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ad827-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-216">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="ad827-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ad827-217">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ad827-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ad827-218">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad827-218">Remarks</span></span>

<span data-ttu-id="ad827-219">L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="ad827-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ad827-220">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ad827-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ad827-221">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad827-221">Examples</span></span>

<span data-ttu-id="ad827-222">Nell'esempio C# seguente vengono visualizzate le informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="ad827-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="ad827-223">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ad827-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad827-224">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="ad827-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="ad827-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad827-225">Requirements</span></span>



| <span data-ttu-id="ad827-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad827-226">Requirement</span></span> | <span data-ttu-id="ad827-227">Valore</span><span class="sxs-lookup"><span data-stu-id="ad827-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad827-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad827-228">Minimum supported client</span></span><br/> | <span data-ttu-id="ad827-229">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ad827-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ad827-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad827-230">Minimum supported server</span></span><br/> | <span data-ttu-id="ad827-231">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ad827-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad827-232">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad827-232">Namespace</span></span><br/>                | <span data-ttu-id="ad827-233">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ad827-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ad827-234">MOF</span><span class="sxs-lookup"><span data-stu-id="ad827-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad827-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad827-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad827-236">DLL</span><span class="sxs-lookup"><span data-stu-id="ad827-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad827-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad827-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad827-238">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad827-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad827-239">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ad827-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="ad827-240">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad827-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ad827-241">**\_SummaryInformation MSVM**</span><span class="sxs-lookup"><span data-stu-id="ad827-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

