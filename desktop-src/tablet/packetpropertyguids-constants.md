---
description: Definisce i valori che specificano le proprietà del pacchetto.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Costanti PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233863"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="9b037-103">Costanti PacketPropertyGuids</span><span class="sxs-lookup"><span data-stu-id="9b037-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="9b037-104">Definisce i valori che specificano le proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9b037-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="9b037-105">Il tablet PCAPI usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in COM sono stringhe costanti.</span><span class="sxs-lookup"><span data-stu-id="9b037-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="9b037-106">In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut. h, che si trova nella <systemdrive> \\ Directory: programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include directory se è stato installato l'SDK nel percorso predefinito.</span><span class="sxs-lookup"><span data-stu-id="9b037-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="9b037-107">In C++, queste costanti sono WCHAR, non BSTR.</span><span class="sxs-lookup"><span data-stu-id="9b037-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="9b037-108">Convertirli in BSTR prima di usarli.</span><span class="sxs-lookup"><span data-stu-id="9b037-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="9b037-109">Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="9b037-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="9b037-110">La tabella seguente elenca i campi GUID (Globally Unique Identifier) delle proprietà dei pacchetti disponibili.</span><span class="sxs-lookup"><span data-stu-id="9b037-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="9b037-111">Usare questi GUID per specificare le proprietà contenute nel pacchetto quando si crea il contesto della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="9b037-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="9b037-112">Per determinare l'intervallo e la risoluzione di una proprietà, chiamare il metodo [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) .</span><span class="sxs-lookup"><span data-stu-id="9b037-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="9b037-113">Le costanti della tabella seguente che iniziano con "STR \_ " sono rappresentazioni di stringa delle costanti binarie corrispondenti mostrate nella stessa cella della tabella.</span><span class="sxs-lookup"><span data-stu-id="9b037-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9b037-114">Costante</span><span class="sxs-lookup"><span data-stu-id="9b037-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9b037-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b037-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="9b037-116"><dt><strong>STR_GUID_X o GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-117">Coordinata x nello spazio delle coordinate della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="9b037-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="9b037-118">Per impostazione predefinita, ogni pacchetto contiene questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b037-118">Each packet contains this property by default.</span></span> <span data-ttu-id="9b037-119">L'origine (0, 0) del tablet è l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="9b037-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="9b037-120"><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-121">Coordinata y nello spazio delle coordinate della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="9b037-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="9b037-122">Per impostazione predefinita, ogni pacchetto contiene questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b037-122">Each packet contains this property by default.</span></span> <span data-ttu-id="9b037-123">L'origine (0, 0) del tablet è l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="9b037-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="9b037-124"><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-125">Coordinata y nello spazio delle coordinate della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="9b037-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="9b037-126">Per impostazione predefinita, ogni pacchetto contiene questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b037-126">Each packet contains this property by default.</span></span> <span data-ttu-id="9b037-127">L'origine (0, 0) del tablet è l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="9b037-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="9b037-128"><dt><strong>STR_GUID_Z o GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-129">Coordinata z o distanza della punta della penna dalla superficie del tablet.</span><span class="sxs-lookup"><span data-stu-id="9b037-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="9b037-130">Il tipo di enumerazione <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> determina l'unità di misura per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b037-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="9b037-131"><dt><strong>STR_GUID_PAKETSTATUS o GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-132">Contiene uno o più dei seguenti valori di flag:</span><span class="sxs-lookup"><span data-stu-id="9b037-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="9b037-133">Il cursore sta toccando la superficie di disegno (valore = 1).</span><span class="sxs-lookup"><span data-stu-id="9b037-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="9b037-134">Il cursore viene invertito.</span><span class="sxs-lookup"><span data-stu-id="9b037-134">The cursor is inverted.</span></span> <span data-ttu-id="9b037-135">Ad esempio, l'estremità della gomma della penna è rivolta verso la superficie (valore = 2).</span><span class="sxs-lookup"><span data-stu-id="9b037-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="9b037-136">Non usato (valore = 4).</span><span class="sxs-lookup"><span data-stu-id="9b037-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="9b037-137">Il pulsante a barilotto è premuto (valore = 8).</span><span class="sxs-lookup"><span data-stu-id="9b037-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="9b037-138"><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-139">Ora di generazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9b037-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="9b037-140"><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-141">Ora di generazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9b037-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="9b037-142"><dt><strong>STR_GUID_SERIALNUMBER o GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-143">Proprietà del pacchetto per l'identificazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9b037-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="9b037-144">Si tratta dello stesso valore usato per recuperare il pacchetto dalla coda di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9b037-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="9b037-145"><dt><strong>STR_GUID_NORMALPRESSURE o GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-146">Pressione della punta della penna perpendicolare alla superficie del tablet.</span><span class="sxs-lookup"><span data-stu-id="9b037-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="9b037-147">Maggiore è la pressione sulla punta della penna, maggiore è l'input penna disegnato.</span><span class="sxs-lookup"><span data-stu-id="9b037-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="9b037-148"><dt><strong>STR_GUID_TANGENTPRESSURE o GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-149">Pressione della punta della penna lungo il piano della superficie della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="9b037-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="9b037-150"><dt><strong>STR_GUID_BUTTONPRESSURE o GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-151">Pressione su un pulsante sensibile alla pressione.</span><span class="sxs-lookup"><span data-stu-id="9b037-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="9b037-152"><dt><strong>STR_GUID_XTILTORIENTATION o GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-153">Angolo tra le y, il piano z e il piano dell'asse y e della penna.</span><span class="sxs-lookup"><span data-stu-id="9b037-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="9b037-154">Si applica a un cursore della penna.</span><span class="sxs-lookup"><span data-stu-id="9b037-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="9b037-155">Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positivo quando la penna è a destra di perpendicolare.</span><span class="sxs-lookup"><span data-stu-id="9b037-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="9b037-156"><dt><strong>STR_GUID_YTILTORIENTATION o GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-157">Angolo tra le x, il piano z e il piano dell'asse x e della penna.</span><span class="sxs-lookup"><span data-stu-id="9b037-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="9b037-158">Si applica a un cursore della penna.</span><span class="sxs-lookup"><span data-stu-id="9b037-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="9b037-159">Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o verso il basso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9b037-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="9b037-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION o GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-161">Rotazione in senso orario del cursore sull'asse z tramite un intervallo circolare completo.</span><span class="sxs-lookup"><span data-stu-id="9b037-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="9b037-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION o GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-163">Angolo tra l'asse della penna e la superficie della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="9b037-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="9b037-164">Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie.</span><span class="sxs-lookup"><span data-stu-id="9b037-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="9b037-165">I valori sono negativi quando la penna è invertita.</span><span class="sxs-lookup"><span data-stu-id="9b037-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="9b037-166"><dt><strong>STR_GUID_TWISTORIENTATION o GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-167">Rotazione in senso orario del cursore sul relativo asse.</span><span class="sxs-lookup"><span data-stu-id="9b037-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="9b037-168"><dt><strong>STR_GUID_PITCHROTATION o GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-169">Proprietà del pacchetto che indica se il suggerimento si trova al di sopra o al di sotto di una linea orizzontale perpendicolare alla superficie di scrittura.</span><span class="sxs-lookup"><span data-stu-id="9b037-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9b037-170">Questa operazione richiede un digitalizzatore 3D.</span><span class="sxs-lookup"><span data-stu-id="9b037-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="9b037-171">Il valore è positivo se il suggerimento si trova sopra la linea e negativo se è sotto la linea.</span><span class="sxs-lookup"><span data-stu-id="9b037-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="9b037-172">Se, ad esempio, si tiene la penna davanti all'utente e si scrive su una parete immaginaria, il pitch è positivo se il suggerimento si trova sopra una riga che si estende dall'utente alla parete.</span><span class="sxs-lookup"><span data-stu-id="9b037-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="9b037-173"><dt><strong>STR_GUID_ROLLROTATION o GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-174">Rotazione in senso orario della penna intorno al proprio asse.</span><span class="sxs-lookup"><span data-stu-id="9b037-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9b037-175">Questa operazione richiede un digitalizzatore 3D.</span><span class="sxs-lookup"><span data-stu-id="9b037-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="9b037-176"><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-177">Angolo della penna a sinistra o a destra intorno al centro dell'asse orizzontale quando la penna è orizzontale.</span><span class="sxs-lookup"><span data-stu-id="9b037-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9b037-178">Questa operazione richiede un digitalizzatore 3D.</span><span class="sxs-lookup"><span data-stu-id="9b037-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="9b037-179">Se si tiene la penna davanti all'utente e si scrive su una parete immaginaria, l'imbardata zero indica che la penna è perpendicolare alla parete.</span><span class="sxs-lookup"><span data-stu-id="9b037-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="9b037-180">Il valore è negativo se il suggerimento si trova a sinistra della perpendicolare e positivo se il suggerimento è a destra di perpendicolare.</span><span class="sxs-lookup"><span data-stu-id="9b037-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="9b037-181"><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-182">Angolo della penna a sinistra o a destra intorno al centro dell'asse orizzontale quando la penna è orizzontale.</span><span class="sxs-lookup"><span data-stu-id="9b037-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9b037-183">Questa operazione richiede un digitalizzatore 3D.</span><span class="sxs-lookup"><span data-stu-id="9b037-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="9b037-184">Se si tiene la penna davanti all'utente e si scrive su una parete immaginaria, l'imbardata zero indica che la penna è perpendicolare alla parete.</span><span class="sxs-lookup"><span data-stu-id="9b037-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="9b037-185">Il valore è negativo se il suggerimento si trova a sinistra della perpendicolare e positivo se il suggerimento è a destra di perpendicolare.</span><span class="sxs-lookup"><span data-stu-id="9b037-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="9b037-186"><dt><strong>STR_GUID_WIDTH o GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-187">Larghezza dell'area di contatto in un digitalizzatore Touch.</span><span class="sxs-lookup"><span data-stu-id="9b037-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="9b037-188"><dt><strong>STR_GUID_HEIGHT o GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-189">Altezza dell'area di contatto in un digitalizzatore Touch.</span><span class="sxs-lookup"><span data-stu-id="9b037-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="9b037-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE o GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-191">Livello di confidenza del contatto del dito su un digitalizzatore Touch.</span><span class="sxs-lookup"><span data-stu-id="9b037-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="9b037-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID o GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9b037-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b037-193">Identificatore del contatto del dispositivo per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9b037-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="9b037-194">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b037-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9b037-195">Tutti i valori dei pacchetti provenienti dall'hardware del tablet sono numeri interi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9b037-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b037-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b037-196">Requirements</span></span>



| <span data-ttu-id="9b037-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b037-197">Requirement</span></span> | <span data-ttu-id="9b037-198">Valore</span><span class="sxs-lookup"><span data-stu-id="9b037-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b037-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b037-199">Minimum supported client</span></span><br/> | <span data-ttu-id="9b037-200">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9b037-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9b037-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b037-201">Minimum supported server</span></span><br/> | <span data-ttu-id="9b037-202">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9b037-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9b037-203">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b037-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b037-204"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9b037-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b037-205">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b037-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b037-206">**Metodo IsPacketPropertySupported**</span><span class="sxs-lookup"><span data-stu-id="9b037-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="9b037-207">**Metodo GetPropertyMetrics**</span><span class="sxs-lookup"><span data-stu-id="9b037-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="9b037-208">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="9b037-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




