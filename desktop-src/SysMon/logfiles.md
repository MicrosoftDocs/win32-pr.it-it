---
title: Oggetto LogFiles (Isysmon.h)
description: Utilizzare questa classe per gestire una raccolta di uno o più file di log che contengono i dati dei contatori delle prestazioni. Per recuperare l'oggetto, chiamare SystemMonitor. LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- SysMon oggetto LogFiles
- Oggetti LogFiles SysMon, descritti
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475052"
---
# <a name="logfiles-object"></a><span data-ttu-id="5c851-105">LogFiles (oggetto)</span><span class="sxs-lookup"><span data-stu-id="5c851-105">LogFiles object</span></span>

<span data-ttu-id="5c851-106">Utilizzare questa classe per gestire una raccolta di uno o più file di log che contengono i dati dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5c851-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="5c851-107">Per recuperare l'oggetto, chiamare [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md).</span><span class="sxs-lookup"><span data-stu-id="5c851-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="5c851-108">Membri</span><span class="sxs-lookup"><span data-stu-id="5c851-108">Members</span></span>

<span data-ttu-id="5c851-109">L'oggetto **LogFiles** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c851-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="5c851-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="5c851-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c851-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c851-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c851-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5c851-112">Methods</span></span>

<span data-ttu-id="5c851-113">Questi metodi sono disponibili nell'oggetto **LogFiles** .</span><span class="sxs-lookup"><span data-stu-id="5c851-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="5c851-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="5c851-114">Method</span></span>                                          | <span data-ttu-id="5c851-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c851-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c851-116">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="5c851-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="5c851-117">Aggiunge un'istanza di [**LogFileItem**](logfileitem.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c851-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="5c851-118">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="5c851-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="5c851-119">Rimuove un'istanza di [**LogFileItem**](logfileitem.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c851-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5c851-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c851-120">Properties</span></span>

<span data-ttu-id="5c851-121">L'oggetto **LogFiles** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c851-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="5c851-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c851-122">Property</span></span>                                                 | <span data-ttu-id="5c851-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c851-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c851-124">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="5c851-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="5c851-125">Recupera il numero di istanze di [**LogFileItem**](logfileitem.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="5c851-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="5c851-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5c851-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="5c851-127">Recupera l'istanza di [**LogFileItem**](logfileitem.md) specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c851-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c851-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c851-128">Remarks</span></span>

<span data-ttu-id="5c851-129">Per visualizzare i contatori delle prestazioni di SYSMON da un file di log, impostare [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) su [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="5c851-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="5c851-130">Dopo l'aggiunta dei file di log alla raccolta, utilizzare la raccolta dei [**contatori**](counters.md) per specificare i dati dei contatori che si desidera leggere dai file di log.</span><span class="sxs-lookup"><span data-stu-id="5c851-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="5c851-131">Si noti che se **SystemMonitor. DataSourceType** è impostato su **DataSourceTypeConstants.sysmonLogFiles**, Sysmon Ricampiona i file di log ogni volta che si aggiunge un file di log o un contatore alle rispettive raccolte.</span><span class="sxs-lookup"><span data-stu-id="5c851-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="5c851-132">**Prima di Windows Vista:** Non è possibile aggiungere file di log alla [**raccolta di file di log**](systemmonitor-logfiles.md) se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="5c851-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="5c851-133">Per prima cosa, impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonNullDataSource**, aggiungere i file di log e i contatori, quindi impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="5c851-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="5c851-134">Le proprietà [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) specificano l'intervallo di valori campionati dai file di log a Graph.</span><span class="sxs-lookup"><span data-stu-id="5c851-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="5c851-135">SYSMON disegna un solo valore di visualizzazione dei dati dal file di log (la visualizzazione del grafico non scorre come quando si crea un grafico dell'attività corrente del computer).</span><span class="sxs-lookup"><span data-stu-id="5c851-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="5c851-136">Se i dati campionati superano quelli che possono essere visualizzati in una singola visualizzazione grafico, SYSMON comprime i dati campionati (ogni punto grafico rappresenta la media di più valori campionati) per adattarsi a tutti i dati campionati dei file di log nel grafico.</span><span class="sxs-lookup"><span data-stu-id="5c851-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c851-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c851-137">Requirements</span></span>



| <span data-ttu-id="5c851-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c851-138">Requirement</span></span> | <span data-ttu-id="5c851-139">Valore</span><span class="sxs-lookup"><span data-stu-id="5c851-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c851-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c851-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5c851-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c851-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5c851-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c851-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5c851-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c851-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c851-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c851-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c851-145"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c851-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5c851-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5c851-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c851-147"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5c851-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





