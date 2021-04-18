---
description: L'oggetto DeviceInfo fornisce l'accesso alle proprietà di un dispositivo hardware Windows Image Acquisition (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Oggetto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312440"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="148be-103">Oggetto DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="148be-103">DeviceInfo object</span></span>

<span data-ttu-id="148be-104">L'oggetto **deviceInfo** fornisce l'accesso alle proprietà di un dispositivo hardware Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="148be-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="148be-105">Inoltre, tramite il metodo [**create**](-wia-iwiadeviceinfo-create.md) , fornisce un modo per l'applicazione o lo script per la connessione al dispositivo e per ottenere un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="148be-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="148be-106">Usare il metodo [**Devices**](-wia-iwia-devices.md) per ottenere una raccolta di oggetti **deviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="148be-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="148be-107">Membri</span><span class="sxs-lookup"><span data-stu-id="148be-107">Members</span></span>

<span data-ttu-id="148be-108">L'oggetto **deviceInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="148be-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="148be-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="148be-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="148be-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="148be-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="148be-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="148be-111">Methods</span></span>

<span data-ttu-id="148be-112">L'oggetto **deviceInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="148be-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="148be-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="148be-113">Method</span></span>                                                 | <span data-ttu-id="148be-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="148be-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="148be-115">**Creare**</span><span class="sxs-lookup"><span data-stu-id="148be-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="148be-116">Il metodo [**create**](-wia-iwiadeviceinfo-create.md) dell'oggetto **deviceInfo** esegue una connessione al dispositivo WIA specificato dall'oggetto **deviceInfo** e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="148be-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="148be-117">**GetPropById**</span><span class="sxs-lookup"><span data-stu-id="148be-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="148be-118">Il metodo [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) dell'oggetto **DEVICEINFO** usa l'ID di una proprietà del dispositivo per restituirne il valore.</span><span class="sxs-lookup"><span data-stu-id="148be-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="148be-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="148be-119">Properties</span></span>

<span data-ttu-id="148be-120">L'oggetto **deviceInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="148be-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="148be-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="148be-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="148be-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="148be-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="148be-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="148be-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="148be-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>ID</strong></a></span><span class="sxs-lookup"><span data-stu-id="148be-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="148be-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-126">Recupera l'ID del dispositivo hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="148be-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="148be-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Produttore</strong></a></span><span class="sxs-lookup"><span data-stu-id="148be-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="148be-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-129">Recupera il nome del produttore del dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="148be-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="148be-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Nome</strong></a></span><span class="sxs-lookup"><span data-stu-id="148be-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="148be-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-132">Nome del dispositivo hardware WIA così come appare nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="148be-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="148be-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Porta</strong></a></span><span class="sxs-lookup"><span data-stu-id="148be-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="148be-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-135">Recupera la porta a cui è connessa la periferica hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="148be-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="148be-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a></span><span class="sxs-lookup"><span data-stu-id="148be-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="148be-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-138">Recupera il tipo di dispositivo hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="148be-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="148be-139">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="148be-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="148be-140">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="148be-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="148be-141">Scanner</span><span class="sxs-lookup"><span data-stu-id="148be-141">Scanner</span></span></li>
<li><span data-ttu-id="148be-142">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="148be-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="148be-143">Predefinito</span><span class="sxs-lookup"><span data-stu-id="148be-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="148be-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span><span class="sxs-lookup"><span data-stu-id="148be-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-145">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="148be-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="148be-146">Recupera l'ID di classe dell'interfaccia utente fornita dal produttore per questo dispositivo hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="148be-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="148be-147">Il valore è una rappresentazione in forma di stringa di un GUID.</span><span class="sxs-lookup"><span data-stu-id="148be-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="148be-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="148be-148">Requirements</span></span>



| <span data-ttu-id="148be-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="148be-149">Requirement</span></span> | <span data-ttu-id="148be-150">Valore</span><span class="sxs-lookup"><span data-stu-id="148be-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="148be-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="148be-151">Minimum supported client</span></span><br/> | <span data-ttu-id="148be-152">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="148be-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="148be-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="148be-153">Minimum supported server</span></span><br/> | <span data-ttu-id="148be-154">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="148be-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="148be-155">DLL</span><span class="sxs-lookup"><span data-stu-id="148be-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="148be-156"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="148be-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




