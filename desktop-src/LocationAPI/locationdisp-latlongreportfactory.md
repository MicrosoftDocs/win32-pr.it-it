---
description: Gestisce i report di Latitudine/Longitudine.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Oggetto LocationDisp. LatLongReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885537"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="a59dc-103">Oggetto LocationDisp. LatLongReportFactory</span><span class="sxs-lookup"><span data-stu-id="a59dc-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="a59dc-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a59dc-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a59dc-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a59dc-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a59dc-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a59dc-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a59dc-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a59dc-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a59dc-108">Gestisce i report di Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="a59dc-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="a59dc-109">Membri</span><span class="sxs-lookup"><span data-stu-id="a59dc-109">Members</span></span>

<span data-ttu-id="a59dc-110">L'oggetto **LocationDisp. LatLongReportFactory** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a59dc-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="a59dc-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a59dc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a59dc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a59dc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a59dc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a59dc-113">Methods</span></span>

<span data-ttu-id="a59dc-114">L'oggetto **LocationDisp. LatLongReportFactory** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a59dc-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="a59dc-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a59dc-115">Method</span></span>                                                                                       | <span data-ttu-id="a59dc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a59dc-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a59dc-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="a59dc-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="a59dc-118">Richiede gli eventi del rapporto Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="a59dc-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="a59dc-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="a59dc-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="a59dc-120">Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.</span><span class="sxs-lookup"><span data-stu-id="a59dc-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="a59dc-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a59dc-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="a59dc-122">Annulla le richieste per gli eventi del report di Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="a59dc-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="a59dc-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a59dc-123">Properties</span></span>

<span data-ttu-id="a59dc-124">Le proprietà dell'oggetto **LocationDisp. LatLongReportFactory** sono queste.</span><span class="sxs-lookup"><span data-stu-id="a59dc-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="a59dc-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a59dc-125">Property</span></span>                                                                                | <span data-ttu-id="a59dc-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a59dc-126">Access type</span></span>           | <span data-ttu-id="a59dc-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a59dc-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a59dc-128">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="a59dc-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="a59dc-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a59dc-129">Read/write</span></span><br/> | <span data-ttu-id="a59dc-130">Valore di accuratezza desiderata corrente.</span><span class="sxs-lookup"><span data-stu-id="a59dc-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="a59dc-131">**LatLongReport**</span><span class="sxs-lookup"><span data-stu-id="a59dc-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="a59dc-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a59dc-132">Read-only</span></span><br/>  | <span data-ttu-id="a59dc-133">[**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)corrente.</span><span class="sxs-lookup"><span data-stu-id="a59dc-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="a59dc-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="a59dc-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="a59dc-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a59dc-135">Read/write</span></span><br/> | <span data-ttu-id="a59dc-136">Intervallo di eventi del report di Latitudine/Longitudine corrente in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a59dc-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="a59dc-137">**Stato**</span><span class="sxs-lookup"><span data-stu-id="a59dc-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="a59dc-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a59dc-138">Read-only</span></span><br/>  | <span data-ttu-id="a59dc-139">Stato corrente del report.</span><span class="sxs-lookup"><span data-stu-id="a59dc-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="a59dc-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="a59dc-140">Examples</span></span>

<span data-ttu-id="a59dc-141">Nell'esempio di codice seguente viene illustrato come creare questo oggetto nel codice HTML.</span><span class="sxs-lookup"><span data-stu-id="a59dc-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="a59dc-142">Nell'esempio di codice seguente viene illustrato come creare questo oggetto in JScript utilizzando Windows script host.</span><span class="sxs-lookup"><span data-stu-id="a59dc-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="a59dc-143">Nell'esempio di codice seguente viene illustrato come creare questo oggetto in VBScript utilizzando Windows script host.</span><span class="sxs-lookup"><span data-stu-id="a59dc-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="a59dc-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a59dc-144">Requirements</span></span>



| <span data-ttu-id="a59dc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="a59dc-145">Requirement</span></span> | <span data-ttu-id="a59dc-146">Valore</span><span class="sxs-lookup"><span data-stu-id="a59dc-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a59dc-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a59dc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a59dc-148">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a59dc-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a59dc-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a59dc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a59dc-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a59dc-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="a59dc-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a59dc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a59dc-152">**LocationDisp.DispLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="a59dc-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

