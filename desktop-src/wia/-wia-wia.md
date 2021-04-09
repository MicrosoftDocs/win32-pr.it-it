---
description: L'oggetto WIA è il punto di ingresso per tutte le funzionalità di scripting di Windows Image Acquisition (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129379"
---
# <a name="wia-object"></a><span data-ttu-id="b1c94-103">WIA (oggetto)</span><span class="sxs-lookup"><span data-stu-id="b1c94-103">Wia object</span></span>

<span data-ttu-id="b1c94-104">L'oggetto **WIA** è il punto di ingresso per tutte le funzionalità di scripting di Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="b1c94-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="b1c94-105">Qualsiasi applicazione che utilizza il modello di scripting WIA deve creare un oggetto [**SafeWia**](-wia-safewia.md) o **WIA** .</span><span class="sxs-lookup"><span data-stu-id="b1c94-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="b1c94-106">Usare tale oggetto per enumerare e creare i dispositivi e ricevere notifiche di eventi hardware.</span><span class="sxs-lookup"><span data-stu-id="b1c94-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="b1c94-107">Questo oggetto non è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="b1c94-107">This object is not safe for scripting.</span></span> <span data-ttu-id="b1c94-108">Per una versione di questo oggetto sicura per gli script, vedere [**SafeWia**](-wia-safewia.md).</span><span class="sxs-lookup"><span data-stu-id="b1c94-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="b1c94-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b1c94-109">Members</span></span>

<span data-ttu-id="b1c94-110">L'oggetto **WIA** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b1c94-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="b1c94-111">Eventi</span><span class="sxs-lookup"><span data-stu-id="b1c94-111">Events</span></span>](#events)
-   [<span data-ttu-id="b1c94-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1c94-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1c94-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1c94-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="b1c94-114">Eventi</span><span class="sxs-lookup"><span data-stu-id="b1c94-114">Events</span></span>

<span data-ttu-id="b1c94-115">L'oggetto **WIA** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="b1c94-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="b1c94-116">Event</span><span class="sxs-lookup"><span data-stu-id="b1c94-116">Event</span></span>                                                                 | <span data-ttu-id="b1c94-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c94-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="b1c94-118">**OnDeviceConnected**</span><span class="sxs-lookup"><span data-stu-id="b1c94-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="b1c94-119">Evento che si verifica quando si connette un nuovo dispositivo hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="b1c94-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="b1c94-120">**OnDeviceDisconnected**</span><span class="sxs-lookup"><span data-stu-id="b1c94-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="b1c94-121">Evento che si verifica quando un nuovo dispositivo hardware WIA viene disconnesso.</span><span class="sxs-lookup"><span data-stu-id="b1c94-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="b1c94-122">**OnTransferComplete**</span><span class="sxs-lookup"><span data-stu-id="b1c94-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="b1c94-123">Evento che si verifica quando un trasferimento dei dati viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1c94-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="b1c94-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1c94-124">Methods</span></span>

<span data-ttu-id="b1c94-125">L'oggetto **WIA** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b1c94-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="b1c94-126">Metodo</span><span class="sxs-lookup"><span data-stu-id="b1c94-126">Method</span></span>                             | <span data-ttu-id="b1c94-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c94-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1c94-128">**Creare**</span><span class="sxs-lookup"><span data-stu-id="b1c94-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="b1c94-129">Il metodo [**create**](-wia-iwia-create.md) dell'oggetto **WIA** esegue una connessione al dispositivo WIA specificato e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1c94-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1c94-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1c94-130">Properties</span></span>

<span data-ttu-id="b1c94-131">L'oggetto **WIA** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1c94-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b1c94-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1c94-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b1c94-133">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b1c94-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b1c94-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c94-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b1c94-135"><a href="-wia-iwia-devices.md"><strong>Dispositivi</strong></a></span><span class="sxs-lookup"><span data-stu-id="b1c94-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b1c94-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b1c94-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="b1c94-137">Raccolta di oggetti <a href="-wia-deviceinfo.md"><strong>deviceInfo</strong></a> che rappresenta tutti i dispositivi installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="b1c94-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="b1c94-138">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b1c94-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b1c94-139">Questa raccolta è in base 0.</span><span class="sxs-lookup"><span data-stu-id="b1c94-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b1c94-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1c94-140">Requirements</span></span>



| <span data-ttu-id="b1c94-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1c94-141">Requirement</span></span> | <span data-ttu-id="b1c94-142">Valore</span><span class="sxs-lookup"><span data-stu-id="b1c94-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c94-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c94-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c94-144">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1c94-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1c94-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c94-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c94-146">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1c94-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b1c94-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b1c94-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1c94-148"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b1c94-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="b1c94-149">IID</span><span class="sxs-lookup"><span data-stu-id="b1c94-149">IID</span></span><br/>                      | <span data-ttu-id="b1c94-150">\_WIA CLSID</span><span class="sxs-lookup"><span data-stu-id="b1c94-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




