---
description: L'oggetto SafeWia è un &\# 0034; Safe per lo scripting&\# 0034; punto di ingresso per tutte le funzionalità di scripting Windows Image Acquisition (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Oggetto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307340"
---
# <a name="safewia-object"></a><span data-ttu-id="398a0-103">Oggetto SafeWia</span><span class="sxs-lookup"><span data-stu-id="398a0-103">SafeWia object</span></span>

<span data-ttu-id="398a0-104">L'oggetto **SafeWia** è un punto di ingresso "Safe per lo scripting" per tutte le funzionalità di scripting Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="398a0-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="398a0-105">Qualsiasi applicazione che utilizza il modello di scripting WIA deve creare un oggetto **SafeWia** o [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="398a0-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="398a0-106">Usare tale oggetto per enumerare e creare i dispositivi e ricevere notifiche di eventi hardware.</span><span class="sxs-lookup"><span data-stu-id="398a0-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="398a0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="398a0-107">Members</span></span>

<span data-ttu-id="398a0-108">L'oggetto **SafeWia** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="398a0-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="398a0-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="398a0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="398a0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="398a0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="398a0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="398a0-111">Methods</span></span>

<span data-ttu-id="398a0-112">L'oggetto **SafeWia** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="398a0-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="398a0-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="398a0-113">Method</span></span>                             | <span data-ttu-id="398a0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="398a0-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="398a0-115">**Creare**</span><span class="sxs-lookup"><span data-stu-id="398a0-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="398a0-116">Il metodo [**create**](-wia-iwia-create.md) dell'oggetto [**WIA**](-wia-wia.md) esegue una connessione al dispositivo WIA specificato e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="398a0-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="398a0-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="398a0-117">Properties</span></span>

<span data-ttu-id="398a0-118">L'oggetto **SafeWia** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="398a0-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="398a0-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="398a0-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="398a0-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="398a0-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="398a0-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="398a0-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="398a0-122"><a href="-wia-iwia-devices.md"><strong>Dispositivi</strong></a></span><span class="sxs-lookup"><span data-stu-id="398a0-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="398a0-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="398a0-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="398a0-124">Raccolta di oggetti <a href="-wia-deviceinfo.md"><strong>deviceInfo</strong></a> che rappresenta tutti i dispositivi installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="398a0-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="398a0-125">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="398a0-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="398a0-126">Questa raccolta è in base 0.</span><span class="sxs-lookup"><span data-stu-id="398a0-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="398a0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="398a0-127">Requirements</span></span>



| <span data-ttu-id="398a0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="398a0-128">Requirement</span></span> | <span data-ttu-id="398a0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="398a0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="398a0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="398a0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="398a0-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="398a0-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="398a0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="398a0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="398a0-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="398a0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="398a0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="398a0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="398a0-135"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="398a0-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="398a0-136">IID</span><span class="sxs-lookup"><span data-stu-id="398a0-136">IID</span></span><br/>                      | <span data-ttu-id="398a0-137">\_SAFEWIA CLSID</span><span class="sxs-lookup"><span data-stu-id="398a0-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="398a0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="398a0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398a0-139">**WIA**</span><span class="sxs-lookup"><span data-stu-id="398a0-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




