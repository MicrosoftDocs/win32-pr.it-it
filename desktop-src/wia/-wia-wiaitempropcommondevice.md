---
description: Oltre alle proprietà delle informazioni sul dispositivo, i dispositivi Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema che le applicazioni leggono e scrivono.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Costanti di proprietà del dispositivo comuni (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526400"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="c9725-103">Costanti della proprietà del dispositivo comune</span><span class="sxs-lookup"><span data-stu-id="c9725-103">Common Device Property Constants</span></span>

<span data-ttu-id="c9725-104">Oltre alle proprietà delle informazioni sul dispositivo, i dispositivi Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema che le applicazioni leggono e scrivono.</span><span class="sxs-lookup"><span data-stu-id="c9725-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="c9725-105">Sono associati all'oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="c9725-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="c9725-106">Le proprietà del dispositivo rappresentano informazioni sul dispositivo, ad esempio lo stato della connessione e l'ora del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9725-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="c9725-107">A ogni proprietà del dispositivo è associata una stringa di proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9725-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="c9725-108">Le costanti della proprietà del dispositivo elencate di seguito sono comuni alla maggior parte o a tutti i dispositivi hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="c9725-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="c9725-109">Il prefisso "WIA \_ DPA \_ " indica una proprietà del dispositivo per tutti i dispositivi e rappresenta la convenzione di denominazione usata in C/C++.</span><span class="sxs-lookup"><span data-stu-id="c9725-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="c9725-110">Per finalità di scripting queste costanti usano il prefisso "Device" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="c9725-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="c9725-111">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="c9725-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c9725-112">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="c9725-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c9725-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9725-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="c9725-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="c9725-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c9725-115">Stato corrente della connessione per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9725-115">The current connection status for the device.</span></span> <span data-ttu-id="c9725-116">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9725-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="c9725-117">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c9725-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="c9725-118">La proprietà può includere i valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9725-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9725-119">Stato connessione</span><span class="sxs-lookup"><span data-stu-id="c9725-119">Connect Status</span></span></th>
<th><span data-ttu-id="c9725-120">Definizione</span><span class="sxs-lookup"><span data-stu-id="c9725-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9725-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="c9725-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="c9725-122">Il dispositivo non è connesso.</span><span class="sxs-lookup"><span data-stu-id="c9725-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9725-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="c9725-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="c9725-124">Il dispositivo è connesso e operativo.</span><span class="sxs-lookup"><span data-stu-id="c9725-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="c9725-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span><span class="sxs-lookup"><span data-stu-id="c9725-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c9725-126">Ora di clock corrente archiviata nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9725-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="c9725-127">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9725-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c9725-128">Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c9725-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="c9725-129">Questa proprietà è supportata solo dai dispositivi che hanno un clock interno.</span><span class="sxs-lookup"><span data-stu-id="c9725-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="c9725-130">Se è possibile impostare l'orologio del dispositivo, questa proprietà è di lettura/scrittura; in caso contrario, è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c9725-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="c9725-131">I dispositivi WIA segnalano l'ora in una struttura <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</span><span class="sxs-lookup"><span data-stu-id="c9725-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="c9725-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="c9725-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c9725-133">Versione del firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9725-133">The device firmware version.</span></span> <span data-ttu-id="c9725-134">Questo valore deve essere un valore stringa, ad esempio &quot; 1.0.4 &quot; o &quot; 1,0 ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="c9725-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="c9725-135">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9725-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="c9725-136">Se il minidriver WIA non fornisce una risorsa di versione, il servizio WIA fornisce il valore &quot; 0.0.0.0 &quot; come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c9725-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="c9725-137">Un'applicazione legge questa proprietà per determinare la versione della DLL di minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="c9725-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="c9725-138">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c9725-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c9725-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9725-139">Requirements</span></span>



| <span data-ttu-id="c9725-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9725-140">Requirement</span></span> | <span data-ttu-id="c9725-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c9725-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9725-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9725-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c9725-143">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9725-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c9725-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9725-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c9725-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9725-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9725-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9725-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9725-147"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9725-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
