---
description: Gestisce i report degli indirizzi civici.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Oggetto LocationDisp. CivicAddressReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758279"
---
# <a name="locationdispcivicaddressreportfactory-object"></a><span data-ttu-id="973f5-103">Oggetto LocationDisp. CivicAddressReportFactory</span><span class="sxs-lookup"><span data-stu-id="973f5-103">LocationDisp.CivicAddressReportFactory object</span></span>

<span data-ttu-id="973f5-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="973f5-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="973f5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="973f5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="973f5-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="973f5-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="973f5-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="973f5-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="973f5-108">Gestisce i report degli indirizzi civici.</span><span class="sxs-lookup"><span data-stu-id="973f5-108">Manages civic address reports.</span></span>

## <a name="members"></a><span data-ttu-id="973f5-109">Membri</span><span class="sxs-lookup"><span data-stu-id="973f5-109">Members</span></span>

<span data-ttu-id="973f5-110">L'oggetto **LocationDisp. CivicAddressReportFactory** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="973f5-110">The **LocationDisp.CivicAddressReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="973f5-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="973f5-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="973f5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="973f5-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="973f5-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="973f5-113">Methods</span></span>

<span data-ttu-id="973f5-114">L'oggetto **LocationDisp. CivicAddressReportFactory** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="973f5-114">The **LocationDisp.CivicAddressReportFactory** object has these methods.</span></span>



| <span data-ttu-id="973f5-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="973f5-115">Method</span></span>                                                                                            | <span data-ttu-id="973f5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="973f5-116">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="973f5-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="973f5-117">**ListenForReports**</span></span>](locationdisp-civicaddressreportfactory-listenforreports.md)               | <span data-ttu-id="973f5-118">Richiede eventi di report relativi all'indirizzo civico.</span><span class="sxs-lookup"><span data-stu-id="973f5-118">Requests civic address report events.</span></span><br/>                                              |
| [<span data-ttu-id="973f5-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="973f5-119">**RequestPermissions**</span></span>](locationdisp-civicaddressreportfactory-requestpermissions.md)           | <span data-ttu-id="973f5-120">Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.</span><span class="sxs-lookup"><span data-stu-id="973f5-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| [<span data-ttu-id="973f5-121">**StopListeningForReports**</span><span class="sxs-lookup"><span data-stu-id="973f5-121">**StopListeningForReports**</span></span>](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | <span data-ttu-id="973f5-122">Annulla le richieste di eventi del report di indirizzo civico.</span><span class="sxs-lookup"><span data-stu-id="973f5-122">Cancels civic address report event requests.</span></span><br/>                                       |



 

### <a name="properties"></a><span data-ttu-id="973f5-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="973f5-123">Properties</span></span>

<span data-ttu-id="973f5-124">Le proprietà dell'oggetto **LocationDisp. CivicAddressReportFactory** sono queste.</span><span class="sxs-lookup"><span data-stu-id="973f5-124">The **LocationDisp.CivicAddressReportFactory** object has these properties.</span></span>



| <span data-ttu-id="973f5-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="973f5-125">Property</span></span>                                                                                        | <span data-ttu-id="973f5-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="973f5-126">Access type</span></span>           | <span data-ttu-id="973f5-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="973f5-127">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="973f5-128">**CivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="973f5-128">**CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | <span data-ttu-id="973f5-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="973f5-129">Read-only</span></span><br/>  | <span data-ttu-id="973f5-130">[**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="973f5-130">The current [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md).</span></span><br/> |
| [<span data-ttu-id="973f5-131">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="973f5-131">**DesiredAccuracy**</span></span>](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | <span data-ttu-id="973f5-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="973f5-132">Read/write</span></span><br/> | <span data-ttu-id="973f5-133">Impostazione di accuratezza desiderata corrente.</span><span class="sxs-lookup"><span data-stu-id="973f5-133">The current desired-accuracy setting.</span></span><br/>                                                           |
| [<span data-ttu-id="973f5-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="973f5-134">**ReportInterval**</span></span>](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | <span data-ttu-id="973f5-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="973f5-135">Read/write</span></span><br/> | <span data-ttu-id="973f5-136">Intervallo di eventi del rapporto di indirizzo civico corrente in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="973f5-136">The current civic address report event interval in milliseconds.</span></span><br/>                                |
| [<span data-ttu-id="973f5-137">**Stato**</span><span class="sxs-lookup"><span data-stu-id="973f5-137">**Status**</span></span>](locationdisp-civicaddressreportfactory-status.md)<br/>                      | <span data-ttu-id="973f5-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="973f5-138">Read-only</span></span><br/>  | <span data-ttu-id="973f5-139">Stato corrente del report.</span><span class="sxs-lookup"><span data-stu-id="973f5-139">The current report status.</span></span><br/>                                                                      |



 

## <a name="examples"></a><span data-ttu-id="973f5-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="973f5-140">Examples</span></span>

<span data-ttu-id="973f5-141">Nell'esempio di codice seguente viene illustrato come creare questo oggetto nel codice HTML.</span><span class="sxs-lookup"><span data-stu-id="973f5-141">The following example code shows how to create this object in HTML code.</span></span>


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="973f5-142">Nell'esempio di codice seguente viene illustrato come creare questo oggetto in JScript utilizzando Windows script host.</span><span class="sxs-lookup"><span data-stu-id="973f5-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



<span data-ttu-id="973f5-143">Nell'esempio di codice seguente viene illustrato come creare questo oggetto in VBScript utilizzando Windows script host.</span><span class="sxs-lookup"><span data-stu-id="973f5-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="973f5-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="973f5-144">Requirements</span></span>



| <span data-ttu-id="973f5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="973f5-145">Requirement</span></span> | <span data-ttu-id="973f5-146">Valore</span><span class="sxs-lookup"><span data-stu-id="973f5-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="973f5-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="973f5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="973f5-148">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="973f5-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="973f5-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="973f5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="973f5-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="973f5-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="973f5-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="973f5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="973f5-152">**LocationDisp.CivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="973f5-152">**LocationDisp.CivicAddressReport**</span></span>](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

