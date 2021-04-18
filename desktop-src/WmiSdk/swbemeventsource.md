---
description: L'oggetto SWbemEventSource recupera gli eventi da una query di eventi insieme a SWbemServices.ExecNotificationQuery.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Oggetto SWbemEventSource (wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309850"
---
# <a name="swbemeventsource-object"></a><span data-ttu-id="80963-103">Oggetto SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="80963-103">SWbemEventSource object</span></span>

<span data-ttu-id="80963-104">L'oggetto **SWbemEventSource** recupera gli eventi da una query di eventi insieme a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="80963-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="80963-105">Si ottiene un oggetto **SWbemEventSource** se si effettua una chiamata a **SWbemServices.ExecNotificationQuery** per creare una query di eventi.</span><span class="sxs-lookup"><span data-stu-id="80963-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="80963-106">È quindi possibile usare il metodo [**NextEvent**](swbemeventsource-nextevent.md) per recuperare gli eventi man mano che arrivano.</span><span class="sxs-lookup"><span data-stu-id="80963-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="80963-107">Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="80963-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="80963-108">Membri</span><span class="sxs-lookup"><span data-stu-id="80963-108">Members</span></span>

<span data-ttu-id="80963-109">L'oggetto **SWbemEventSource** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="80963-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="80963-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="80963-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="80963-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80963-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="80963-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="80963-112">Methods</span></span>

<span data-ttu-id="80963-113">L'oggetto **SWbemEventSource** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="80963-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="80963-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="80963-114">Method</span></span>                                          | <span data-ttu-id="80963-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80963-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80963-116">**NextEvent**</span><span class="sxs-lookup"><span data-stu-id="80963-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="80963-117">Utilizzato per recuperare un evento in combinazione con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="80963-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="80963-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80963-118">Properties</span></span>

<span data-ttu-id="80963-119">L'oggetto **SWbemEventSource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="80963-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="80963-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80963-120">Property</span></span>                                                    | <span data-ttu-id="80963-121">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="80963-121">Access type</span></span>          | <span data-ttu-id="80963-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80963-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="80963-123">**Sicurezza\_**</span><span class="sxs-lookup"><span data-stu-id="80963-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="80963-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="80963-124">Read-only</span></span><br/> | <span data-ttu-id="80963-125">Utilizzato per leggere o modificare le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="80963-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="80963-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="80963-126">Examples</span></span>

<span data-ttu-id="80963-127">Questo script usa i metodi della classe **SWbemEventSource** e la classe [**SWbemServices**](swbemservices.md) insieme a una query WQL per gli eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80963-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="80963-128">Per ulteriori informazioni sulla notifica degli eventi WMI e sulle query, vedere [eventi di monitoraggio](monitoring-events.md), [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)e [ricezione di notifiche di eventi asincroni](receiving-asynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="80963-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a><span data-ttu-id="80963-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80963-129">Requirements</span></span>



| <span data-ttu-id="80963-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="80963-130">Requirement</span></span> | <span data-ttu-id="80963-131">Valore</span><span class="sxs-lookup"><span data-stu-id="80963-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80963-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80963-132">Minimum supported client</span></span><br/> | <span data-ttu-id="80963-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80963-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80963-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80963-134">Minimum supported server</span></span><br/> | <span data-ttu-id="80963-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80963-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80963-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80963-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="80963-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="80963-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="80963-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="80963-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="80963-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="80963-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="80963-140">DLL</span><span class="sxs-lookup"><span data-stu-id="80963-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80963-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80963-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="80963-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="80963-142">CLSID</span></span><br/>                    | <span data-ttu-id="80963-143">\_SWBEMEVENTSOURCE CLSID</span><span class="sxs-lookup"><span data-stu-id="80963-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="80963-144">IID</span><span class="sxs-lookup"><span data-stu-id="80963-144">IID</span></span><br/>                      | <span data-ttu-id="80963-145">\_ISWBEMEVENTSOURCE IID</span><span class="sxs-lookup"><span data-stu-id="80963-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="80963-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80963-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80963-147">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="80963-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

