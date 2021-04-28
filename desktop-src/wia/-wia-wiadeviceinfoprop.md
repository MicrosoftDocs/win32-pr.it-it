---
description: "Costanti delle proprietà relative alle informazioni sul dispositivo : le proprietà relative alle informazioni sul dispositivo sono proprietà che descrivono la configurazione e l'installazione del dispositivo."
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Costanti della proprietà Device Information (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aec37ae84eed6b15bc10a4e979a5d95d21be3423
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097239"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="8d16f-103">Costanti delle proprietà relative alle informazioni sul dispositivo</span><span class="sxs-lookup"><span data-stu-id="8d16f-103">Device Information Property Constants</span></span>

<span data-ttu-id="8d16f-104">Le proprietà relative alle informazioni sul dispositivo sono proprietà che descrivono la configurazione e l'installazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="8d16f-105">Queste proprietà sono disponibili tramite le [**interfacce IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e anche tramite l'elemento radice.</span><span class="sxs-lookup"><span data-stu-id="8d16f-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="8d16f-106">Le proprietà relative alle informazioni sul dispositivo sono precedute dal prefisso "WIA DIP" (proprietà Device Information) e vengono fornite da \_ \_ Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="8d16f-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="8d16f-107">A scopo di scripting, queste costanti usano il prefisso "DeviceInfo" e fanno parte del tipo [enumerato WiaDeviceInfoPropertyId.](-wia-wiadeviceinfopropertyid.md)</span><span class="sxs-lookup"><span data-stu-id="8d16f-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="8d16f-108">Il nome del membro corrispondente dell'enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="8d16f-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8d16f-109">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="8d16f-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8d16f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d16f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="8d16f-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d16f-112">Stringa ID dispositivo per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="8d16f-113">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="8d16f-114">Tipo: VT_BSTR, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="8d16f-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d16f-116">Stringa di descrizione del fornitore per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="8d16f-117">La descrizione del fornitore viene ottenuta dal file INF.</span><span class="sxs-lookup"><span data-stu-id="8d16f-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="8d16f-118">Un'applicazione legge questa proprietà per ottenere una descrizione del fornitore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="8d16f-119">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="8d16f-120">Tipo: VT_BSTR, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="8d16f-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d16f-122">Stringa di descrizione del dispositivo per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="8d16f-123">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-124">La stringa di descrizione del dispositivo contenuta in questa proprietà viene ottenuta dal file INF.</span><span class="sxs-lookup"><span data-stu-id="8d16f-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="8d16f-125">Un'applicazione legge questa proprietà per ottenere una descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="8d16f-126">Tipo: VT_BSTR, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="8d16f-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d16f-128">Tipo di dispositivo e sottotipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-128">The device type and device subtype.</span></span> <span data-ttu-id="8d16f-129">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-130">Usare la macro GET_STIDEVICE_TYPE per ottenere il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="8d16f-131">Il tipo di dispositivo e il sottotipo vengono ottenuti dal file INF.</span><span class="sxs-lookup"><span data-stu-id="8d16f-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="8d16f-132">Un'applicazione legge questa proprietà per determinare se usa uno scanner, una fotocamera o un dispositivo video.</span><span class="sxs-lookup"><span data-stu-id="8d16f-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="8d16f-133">Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="8d16f-134">Attualmente, i tipi di dispositivo sono definiti come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8d16f-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="8d16f-135">L'asterisco \* indica che il tipo di dispositivo non è supportato da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="8d16f-136">Il doppio asterisco \*\* indica che il tipo di dispositivo non è supportato da Windows Server 2003, Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d16f-137">Type</span><span class="sxs-lookup"><span data-stu-id="8d16f-137">Type</span></span></th>
<th><span data-ttu-id="8d16f-138">valore</span><span class="sxs-lookup"><span data-stu-id="8d16f-138">Value</span></span></th>
<th><span data-ttu-id="8d16f-139">Definizione</span><span class="sxs-lookup"><span data-stu-id="8d16f-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d16f-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="8d16f-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="8d16f-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="8d16f-141">0x0000</span></span></td>
<td><span data-ttu-id="8d16f-142">Dispositivo predefinito</span><span class="sxs-lookup"><span data-stu-id="8d16f-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d16f-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="8d16f-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="8d16f-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="8d16f-144">0x0001</span></span></td>
<td><span data-ttu-id="8d16f-145">Dispositivo scanner (vedere il <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> per determinare se lo scanner è a schermo piatto o alimentato a fogli).</span><span class="sxs-lookup"><span data-stu-id="8d16f-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d16f-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="8d16f-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="8d16f-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="8d16f-147">0x0002</span></span></td>
<td><span data-ttu-id="8d16f-148">Dispositivo fotocamera</span><span class="sxs-lookup"><span data-stu-id="8d16f-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d16f-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="8d16f-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="8d16f-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="8d16f-150">0x0003</span></span></td>
<td><span data-ttu-id="8d16f-151">Dispositivo video</span><span class="sxs-lookup"><span data-stu-id="8d16f-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="8d16f-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-153">Nome della porta del dispositivo installato, assegnato dal driver in modalità kernel che gestisce il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="8d16f-154">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-155">Un'applicazione legge questa proprietà per determinare il nome della porta.</span><span class="sxs-lookup"><span data-stu-id="8d16f-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="8d16f-156">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="8d16f-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-158">Nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-158">The name of the device.</span></span> <span data-ttu-id="8d16f-159">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-160">Il nome del dispositivo contenuto in questa proprietà viene ottenuto dal file INF.</span><span class="sxs-lookup"><span data-stu-id="8d16f-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="8d16f-161">Un'applicazione legge questa proprietà per ottenere il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="8d16f-162">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="8d16f-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-164">Nome del server in cui è in esecuzione il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="8d16f-165">Questa proprietà è facoltativa per Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="8d16f-166">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="8d16f-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-168">ID del dispositivo WIA installato in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="8d16f-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="8d16f-169">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-170">Viene usato solo internamente dal servizio WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="8d16f-171">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="8d16f-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-173">CLSID fornito dal fornitore per qualsiasi oggetto COM dell'estensione dell'interfaccia utente installato con il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="8d16f-174">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-175">Il valore CLSID dell'interfaccia utente contenuto in questa proprietà viene ottenuto dal file INF.</span><span class="sxs-lookup"><span data-stu-id="8d16f-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="8d16f-176">Se non viene specificato alcun CLSID dell'interfaccia utente, il servizio WIA fornisce un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8d16f-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="8d16f-177">Questa proprietà viene usata solo internamente dal servizio WIA quando viene visualizzata l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="8d16f-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="8d16f-178">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="8d16f-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-180">Tipo di connessione utilizzato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-180">The type of connection that the device is using.</span></span> <span data-ttu-id="8d16f-181">Il servizio WIA crea e gestisce questa proprietà e solo il servizio WIA può modificarla.</span><span class="sxs-lookup"><span data-stu-id="8d16f-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="8d16f-182">Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="8d16f-183">La proprietà può avere i valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8d16f-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d16f-184">valore</span><span class="sxs-lookup"><span data-stu-id="8d16f-184">Value</span></span></th>
<th><span data-ttu-id="8d16f-185">Definizione</span><span class="sxs-lookup"><span data-stu-id="8d16f-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d16f-186">1</span><span class="sxs-lookup"><span data-stu-id="8d16f-186">1</span></span></td>
<td><span data-ttu-id="8d16f-187">Dispositivo WDM generico</span><span class="sxs-lookup"><span data-stu-id="8d16f-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d16f-188">2</span><span class="sxs-lookup"><span data-stu-id="8d16f-188">2</span></span></td>
<td><span data-ttu-id="8d16f-189">Dispositivo SCSI</span><span class="sxs-lookup"><span data-stu-id="8d16f-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d16f-190">4</span><span class="sxs-lookup"><span data-stu-id="8d16f-190">4</span></span></td>
<td><span data-ttu-id="8d16f-191">Dispositivo USB</span><span class="sxs-lookup"><span data-stu-id="8d16f-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d16f-192">8</span><span class="sxs-lookup"><span data-stu-id="8d16f-192">8</span></span></td>
<td><span data-ttu-id="8d16f-193">Dispositivo seriale</span><span class="sxs-lookup"><span data-stu-id="8d16f-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d16f-194">16</span><span class="sxs-lookup"><span data-stu-id="8d16f-194">16</span></span></td>
<td><span data-ttu-id="8d16f-195">Dispositivo parallelo</span><span class="sxs-lookup"><span data-stu-id="8d16f-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="8d16f-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-197">Impostazione corrente della velocità in baud per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="8d16f-198">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-199">Il valore deve essere &quot; Vuoto se il dispositivo non è connesso tramite un cavo &quot; seriale.</span><span class="sxs-lookup"><span data-stu-id="8d16f-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="8d16f-200">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="8d16f-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-202">Funzionalità sti generiche per il dispositivo ottenute dal file INF.</span><span class="sxs-lookup"><span data-stu-id="8d16f-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="8d16f-203">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-204">Un'applicazione legge questa proprietà per determinare le funzionalità STI generiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="8d16f-205">Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="8d16f-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-207">Numero (come stringa) della versione wi-fi corrente installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8d16f-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="8d16f-208">Un'applicazione legge questa proprietà per determinare la versione di WIA installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8d16f-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="8d16f-209">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-210">Questa proprietà è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="8d16f-211">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="8d16f-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-213">Versione DLL corrente del minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="8d16f-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="8d16f-214">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-215">Questa proprietà è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="8d16f-216">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="8d16f-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-218">ID PnP corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d16f-218">The current PnP id for the device.</span></span> <span data-ttu-id="8d16f-219">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-220">Questa proprietà è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="8d16f-221">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="8d16f-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="8d16f-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d16f-223">Versione generica del driver STI.</span><span class="sxs-lookup"><span data-stu-id="8d16f-223">The generic STI driver version.</span></span> <span data-ttu-id="8d16f-224">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d16f-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="8d16f-225">Un'applicazione legge questa proprietà per determinare la versione generica del driver STI.</span><span class="sxs-lookup"><span data-stu-id="8d16f-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="8d16f-226">Questa proprietà è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8d16f-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="8d16f-227">Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d16f-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="8d16f-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d16f-228">Requirements</span></span>



| <span data-ttu-id="8d16f-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d16f-229">Requirement</span></span> | <span data-ttu-id="8d16f-230">Valore</span><span class="sxs-lookup"><span data-stu-id="8d16f-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d16f-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d16f-231">Minimum supported client</span></span><br/> | <span data-ttu-id="8d16f-232">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8d16f-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8d16f-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d16f-233">Minimum supported server</span></span><br/> | <span data-ttu-id="8d16f-234">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d16f-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d16f-235">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d16f-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d16f-236"><dt>Wiadef.h</dt></span><span class="sxs-lookup"><span data-stu-id="8d16f-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




