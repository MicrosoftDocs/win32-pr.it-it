---
description: I qualificatori seguenti vengono usati dal provider WDM nei file MOF dei driver di dispositivo quando estraggono dati da WNODEs per generare istanze delle classi di driver WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Qualificatori specifici del provider WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308835"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="e4ece-103">Qualificatori specifici del provider WDM</span><span class="sxs-lookup"><span data-stu-id="e4ece-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="e4ece-104">I qualificatori seguenti vengono usati dal [provider WDM](/windows/desktop/WmiCoreProv/wdm-provider) nei file MOF dei driver di dispositivo quando estraggono dati da WNODEs per generare istanze delle classi di driver WDM.</span><span class="sxs-lookup"><span data-stu-id="e4ece-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="e4ece-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span><span class="sxs-lookup"><span data-stu-id="e4ece-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="e4ece-106">Tipo di dati: **DWORD, array, Uint8, UInt16, UInt32, sint8, sint16 o sint32.**</span><span class="sxs-lookup"><span data-stu-id="e4ece-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="e4ece-107">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4ece-107">Applies to: properties</span></span>

<span data-ttu-id="e4ece-108">Un valore mancante per questa proprietà deve essere rappresentato da **null** anziché da 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e4ece-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="e4ece-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span><span class="sxs-lookup"><span data-stu-id="e4ece-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="e4ece-110">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4ece-110">Data type: **uint32**</span></span>

<span data-ttu-id="e4ece-111">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4ece-111">Applies to: properties</span></span>

<span data-ttu-id="e4ece-112">Indice nel WNODE dei dati per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ece-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="e4ece-113">Il provider WDM utilizza questo qualificatore per determinare il modo in cui i dati vengono formattati durante l'estrazione dei dati da WNODE e la generazione di classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e4ece-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="e4ece-114">Il valore iniziale è 1.</span><span class="sxs-lookup"><span data-stu-id="e4ece-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="e4ece-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span><span class="sxs-lookup"><span data-stu-id="e4ece-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="e4ece-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4ece-116">Data type: **uint32**</span></span>

<span data-ttu-id="e4ece-117">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="e4ece-117">Applies to: classes</span></span>

<span data-ttu-id="e4ece-118">Indica il costo della risorsa per accedere al blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="e4ece-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="e4ece-119">Ad esempio, le informazioni di geometria del disco non richiedono numerose risorse da ottenere perché sono disponibili nell'estensione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4ece-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="e4ece-120">Le prestazioni di lettura/scrittura su disco sono molto più complesse perché richiedono un lavoro aggiuntivo per ogni operazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e4ece-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="e4ece-121">Pertanto, il valore del qualificatore **WMIExpense** è maggiore per le prestazioni di lettura/scrittura del disco.</span><span class="sxs-lookup"><span data-stu-id="e4ece-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="e4ece-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span><span class="sxs-lookup"><span data-stu-id="e4ece-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="e4ece-123">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4ece-123">Data type: **uint32**</span></span>

<span data-ttu-id="e4ece-124">Si applica a: metodi</span><span class="sxs-lookup"><span data-stu-id="e4ece-124">Applies to: methods</span></span>

<span data-ttu-id="e4ece-125">Indice nel WNODE dei dati per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ece-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="e4ece-126">Il provider WDM utilizza questo qualificatore per determinare il modo in cui i dati vengono formattati durante l'estrazione dei dati da WNODE e la generazione di classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e4ece-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="e4ece-127">Il valore iniziale è 1.</span><span class="sxs-lookup"><span data-stu-id="e4ece-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4ece-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4ece-128">Requirements</span></span>



| <span data-ttu-id="e4ece-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ece-129">Requirement</span></span> | <span data-ttu-id="e4ece-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ece-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e4ece-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4ece-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ece-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4ece-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e4ece-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4ece-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ece-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4ece-134">Windows Server 2008</span></span><br/> |



 

