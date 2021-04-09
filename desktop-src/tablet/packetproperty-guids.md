---
description: Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti utilizzati dalla struttura di proprietà del pacchetto \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID di PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885573"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="dd939-103">GUID di PacketProperty</span><span class="sxs-lookup"><span data-stu-id="dd939-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="dd939-104">Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti utilizzati dalla struttura di [**\_ proprietà del pacchetto**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .</span><span class="sxs-lookup"><span data-stu-id="dd939-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd939-105">GUID</span><span class="sxs-lookup"><span data-stu-id="dd939-105">GUID</span></span></th>
<th><span data-ttu-id="dd939-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd939-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd939-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="dd939-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="dd939-108">Angolo tra l'asse della penna e la superficie della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="dd939-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="dd939-109">Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie.</span><span class="sxs-lookup"><span data-stu-id="dd939-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="dd939-110">I valori sono negativi quando la penna è invertita.</span><span class="sxs-lookup"><span data-stu-id="dd939-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="dd939-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="dd939-112">Rotazione in senso orario del cursore intorno all'asse z tramite un intervallo circolare completo.</span><span class="sxs-lookup"><span data-stu-id="dd939-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="dd939-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="dd939-114">GUID utilizzato per recuperare il numero di casella per un riconoscimento dell'input penna alternativo quando il riconoscimento funziona in modalità Box.</span><span class="sxs-lookup"><span data-stu-id="dd939-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="dd939-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="dd939-116">Pressione su un pulsante sensibile alla pressione.</span><span class="sxs-lookup"><span data-stu-id="dd939-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="dd939-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="dd939-118">GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna perpendicolare alla superficie del tablet.</span><span class="sxs-lookup"><span data-stu-id="dd939-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="dd939-119">Maggiore è la pressione applicata alla punta della penna, più l'input penna disegnato.</span><span class="sxs-lookup"><span data-stu-id="dd939-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="dd939-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="dd939-121">Contiene uno o più dei seguenti valori di flag:</span><span class="sxs-lookup"><span data-stu-id="dd939-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="dd939-122">Il cursore sta toccando la superficie di disegno (valore = 1).</span><span class="sxs-lookup"><span data-stu-id="dd939-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="dd939-123">Il cursore viene invertito.</span><span class="sxs-lookup"><span data-stu-id="dd939-123">The cursor is inverted.</span></span> <span data-ttu-id="dd939-124">Ad esempio, l'estremità della gomma della penna è rivolta verso la superficie (valore = 2).</span><span class="sxs-lookup"><span data-stu-id="dd939-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="dd939-125">Non usato (valore = 4).</span><span class="sxs-lookup"><span data-stu-id="dd939-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="dd939-126">Il pulsante a barilotto è premuto (valore = 8).</span><span class="sxs-lookup"><span data-stu-id="dd939-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="dd939-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="dd939-128">Identificatore del contatto del dispositivo per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="dd939-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="dd939-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="dd939-130">Identifica il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="dd939-130">Identifies the packet.</span></span> <span data-ttu-id="dd939-131">Si tratta dello stesso valore usato per recuperare il pacchetto dalla coda di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="dd939-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="dd939-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="dd939-133">GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna lungo il piano della superficie della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="dd939-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="dd939-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="dd939-135">Ora di generazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="dd939-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="dd939-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="dd939-137">Rotazione in senso orario del cursore intorno al proprio asse.</span><span class="sxs-lookup"><span data-stu-id="dd939-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="dd939-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="dd939-139">Coordinata x nello spazio delle coordinate della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="dd939-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="dd939-140">Per impostazione predefinita, ogni pacchetto contiene questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd939-140">Each packet contains this property by default.</span></span> <span data-ttu-id="dd939-141">L'origine (0, 0) del tablet è l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="dd939-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="dd939-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="dd939-143">Per un cursore penna, l'orientamento x-Tilt è l'angolo tra il piano y, z e il piano dell'asse y e della penna.</span><span class="sxs-lookup"><span data-stu-id="dd939-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="dd939-144">Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positivo quando la penna è a destra di perpendicolare.</span><span class="sxs-lookup"><span data-stu-id="dd939-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="dd939-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="dd939-146">Coordinata y nello spazio delle coordinate della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="dd939-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="dd939-147">Per impostazione predefinita, ogni pacchetto contiene questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd939-147">Each packet contains this property by default.</span></span> <span data-ttu-id="dd939-148">L'origine (0, 0) del tablet è l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="dd939-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd939-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="dd939-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="dd939-150">Per un cursore penna, l'orientamento y è l'angolo tra il piano x, z e il piano dell'asse x e della penna.</span><span class="sxs-lookup"><span data-stu-id="dd939-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="dd939-151">Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o fuori dall'utente.</span><span class="sxs-lookup"><span data-stu-id="dd939-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd939-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="dd939-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="dd939-153">Coordinata z o distanza della punta della penna dalla superficie del tablet.</span><span class="sxs-lookup"><span data-stu-id="dd939-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="dd939-154">Il tipo di enumerazione <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> determina l'unità di misura per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd939-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="dd939-155">Il campo TangentPressure rappresenta la pressione lungo il piano della superficie del Tablet; il campo NormalPressure rappresenta la pressione perpendicolare al piano della superficie della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="dd939-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 




