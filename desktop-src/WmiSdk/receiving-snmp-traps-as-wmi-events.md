---
description: WMI esegue automaticamente il mapping di trap SNMP a eventi WMI. Il sistema inserisce i dati contenuti nella trap nelle proprietà corrispondenti di un'istanza di evento WMI per l'accesso da parte del computer host WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Ricezione di trap SNMP come eventi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528507"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="4d1a2-104">Ricezione di trap SNMP come eventi WMI</span><span class="sxs-lookup"><span data-stu-id="4d1a2-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="4d1a2-105">WMI esegue automaticamente il mapping di trap SNMP a eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="4d1a2-106">Il sistema inserisce i dati contenuti nella trap nelle proprietà corrispondenti di un'istanza di evento WMI per l'accesso da parte del computer host WMI.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="4d1a2-107">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4d1a2-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="4d1a2-108">La ricezione di un trap SNMP è quasi identica alla ricezione di eventi da qualsiasi altro provider WMI.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="4d1a2-109">Tuttavia, il filtro eventi SNMP dispone di diverse classi univoche da tenere presenti prima di eseguire la registrazione per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="4d1a2-110">Il provider di eventi richiede inoltre l'utilizzo esclusivo dello \\ spazio dei nomi archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="4d1a2-111">Le classi più comuni con cui eseguire la registrazione sono [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md).</span><span class="sxs-lookup"><span data-stu-id="4d1a2-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="4d1a2-112">Gli utenti intenzionati a utilizzare le notifiche degli eventi per aggiornare i valori nei dispositivi SNMP monitorati devono registrarsi per gli eventi SnmpExtendedNotification.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="4d1a2-113">Le informazioni degli eventi SnmpNotification non sono riutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="4d1a2-114">Nella tabella seguente sono elencate le informazioni sulla configurazione del computer per la ricezione di trap SNMP come eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="4d1a2-115">Attività</span><span class="sxs-lookup"><span data-stu-id="4d1a2-115">Task</span></span>                                                                               | <span data-ttu-id="4d1a2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d1a2-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d1a2-117">Scelta tra i provider di eventi SNMP</span><span class="sxs-lookup"><span data-stu-id="4d1a2-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="4d1a2-118">WMI include due provider di eventi SNMP.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="4d1a2-119">Ricezione di eventi SNMP</span><span class="sxs-lookup"><span data-stu-id="4d1a2-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="4d1a2-120">I provider di eventi SNMP supportano tre tipi di trap SNMPv1 e notifiche SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="4d1a2-121">L'esempio seguente configura un computer per monitorare l'evento **SnmpLinkUpNotification** da un hub gestito.</span><span class="sxs-lookup"><span data-stu-id="4d1a2-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



