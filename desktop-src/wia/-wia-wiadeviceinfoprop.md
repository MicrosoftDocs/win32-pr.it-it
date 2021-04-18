---
description: Le proprietà delle informazioni sul dispositivo sono proprietà che descrivono la configurazione e l'installazione del dispositivo.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Costanti di proprietà delle informazioni sul dispositivo (Wiadef. h)
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
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307295"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="5d943-103">Costanti della proprietà informazioni sul dispositivo</span><span class="sxs-lookup"><span data-stu-id="5d943-103">Device Information Property Constants</span></span>

<span data-ttu-id="5d943-104">Le proprietà delle informazioni sul dispositivo sono proprietà che descrivono la configurazione e l'installazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="5d943-105">Queste proprietà sono disponibili tramite le interfacce [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e anche tramite l'elemento radice.</span><span class="sxs-lookup"><span data-stu-id="5d943-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="5d943-106">Le proprietà delle informazioni sul dispositivo sono precedute dal prefisso "WIA \_ DIP \_ " (proprietà informazioni sul dispositivo) e vengono fornite da Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="5d943-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="5d943-107">A scopo di scripting, queste costanti utilizzano il prefisso "DeviceInfo" e fanno parte del tipo enumerato [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="5d943-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="5d943-108">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="5d943-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="5d943-109">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="5d943-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="5d943-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d943-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="5d943-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5d943-112">Stringa dell'ID del dispositivo per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="5d943-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="5d943-113">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="5d943-114">Tipo: VT_BSTR, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="5d943-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5d943-116">Stringa di descrizione del fornitore per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="5d943-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="5d943-117">La descrizione del fornitore è ottenuta dal file INF.</span><span class="sxs-lookup"><span data-stu-id="5d943-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="5d943-118">Un'applicazione legge questa proprietà per ottenere una descrizione del fornitore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="5d943-119">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="5d943-120">Tipo: VT_BSTR, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="5d943-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5d943-122">Stringa di descrizione del dispositivo per il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="5d943-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="5d943-123">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-124">La stringa di descrizione del dispositivo che questa proprietà contiene è ottenuta dal file INF.</span><span class="sxs-lookup"><span data-stu-id="5d943-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="5d943-125">Un'applicazione legge questa proprietà per ottenere una descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="5d943-126">Tipo: VT_BSTR, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="5d943-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5d943-128">Il tipo di dispositivo e il sottotipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-128">The device type and device subtype.</span></span> <span data-ttu-id="5d943-129">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-130">Usare la macro GET_STIDEVICE_TYPE per ottenere il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="5d943-131">Il tipo di dispositivo e il sottotipo vengono ottenuti dal file INF.</span><span class="sxs-lookup"><span data-stu-id="5d943-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="5d943-132">Un'applicazione legge questa proprietà per determinare se usa uno scanner, una fotocamera o un dispositivo video.</span><span class="sxs-lookup"><span data-stu-id="5d943-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="5d943-133">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="5d943-134">Attualmente, i tipi di dispositivo vengono definiti come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5d943-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="5d943-135">L'asterisco \* indica che il tipo di dispositivo non è supportato da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5d943-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="5d943-136">Il doppio asterisco \* \* indica che il tipo di dispositivo non è supportato da Windows Server 2003, Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="5d943-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d943-137">Type</span><span class="sxs-lookup"><span data-stu-id="5d943-137">Type</span></span></th>
<th><span data-ttu-id="5d943-138">valore</span><span class="sxs-lookup"><span data-stu-id="5d943-138">Value</span></span></th>
<th><span data-ttu-id="5d943-139">Definizione</span><span class="sxs-lookup"><span data-stu-id="5d943-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d943-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="5d943-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="5d943-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="5d943-141">0x0000</span></span></td>
<td><span data-ttu-id="5d943-142">Dispositivo predefinito</span><span class="sxs-lookup"><span data-stu-id="5d943-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d943-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="5d943-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="5d943-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="5d943-144">0x0001</span></span></td>
<td><span data-ttu-id="5d943-145">Dispositivo dello scanner (vedere la <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> per determinare se lo scanner è piano o alimentato da foglio).</span><span class="sxs-lookup"><span data-stu-id="5d943-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d943-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="5d943-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="5d943-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="5d943-147">0x0002</span></span></td>
<td><span data-ttu-id="5d943-148">Dispositivo fotocamera</span><span class="sxs-lookup"><span data-stu-id="5d943-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d943-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="5d943-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="5d943-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="5d943-150">0x0003</span></span></td>
<td><span data-ttu-id="5d943-151">Dispositivo video</span><span class="sxs-lookup"><span data-stu-id="5d943-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="5d943-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-153">Nome della porta del dispositivo installato, assegnato dal driver in modalità kernel che gestisce il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="5d943-154">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-155">Un'applicazione legge questa proprietà per determinare il nome della porta.</span><span class="sxs-lookup"><span data-stu-id="5d943-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="5d943-156">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="5d943-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-158">Nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-158">The name of the device.</span></span> <span data-ttu-id="5d943-159">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-160">Il nome del dispositivo contenuto in questa proprietà è ottenuto dal file INF.</span><span class="sxs-lookup"><span data-stu-id="5d943-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="5d943-161">Un'applicazione legge questa proprietà per ottenere il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="5d943-162">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="5d943-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-164">Nome del server su cui è in esecuzione il minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="5d943-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="5d943-165">Questa proprietà è facoltativa per Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5d943-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="5d943-166">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="5d943-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-168">ID dispositivo del dispositivo WIA installato in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="5d943-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="5d943-169">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-170">Viene usato solo internamente dal servizio WIA.</span><span class="sxs-lookup"><span data-stu-id="5d943-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="5d943-171">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="5d943-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-173">Il CLSID fornito dal fornitore per qualsiasi oggetto COM di estensione dell'interfaccia utente installato con WIA minidriver.</span><span class="sxs-lookup"><span data-stu-id="5d943-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="5d943-174">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-175">Il valore CLSID dell'interfaccia utente contenuto in questa proprietà è ottenuto dal file INF.</span><span class="sxs-lookup"><span data-stu-id="5d943-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="5d943-176">Se non viene specificato alcun CLSID dell'interfaccia utente, il servizio WIA fornisce un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5d943-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="5d943-177">Questa proprietà viene utilizzata internamente dal servizio WIA solo quando viene visualizzata l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5d943-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="5d943-178">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="5d943-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-180">Tipo di connessione usata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-180">The type of connection that the device is using.</span></span> <span data-ttu-id="5d943-181">Il servizio WIA crea e gestisce questa proprietà e solo il servizio WIA può modificarlo.</span><span class="sxs-lookup"><span data-stu-id="5d943-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="5d943-182">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="5d943-183">La proprietà può includere i valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="5d943-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d943-184">valore</span><span class="sxs-lookup"><span data-stu-id="5d943-184">Value</span></span></th>
<th><span data-ttu-id="5d943-185">Definizione</span><span class="sxs-lookup"><span data-stu-id="5d943-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d943-186">1</span><span class="sxs-lookup"><span data-stu-id="5d943-186">1</span></span></td>
<td><span data-ttu-id="5d943-187">Dispositivo WDM generico</span><span class="sxs-lookup"><span data-stu-id="5d943-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d943-188">2</span><span class="sxs-lookup"><span data-stu-id="5d943-188">2</span></span></td>
<td><span data-ttu-id="5d943-189">Dispositivo SCSI</span><span class="sxs-lookup"><span data-stu-id="5d943-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d943-190">4</span><span class="sxs-lookup"><span data-stu-id="5d943-190">4</span></span></td>
<td><span data-ttu-id="5d943-191">Dispositivo USB</span><span class="sxs-lookup"><span data-stu-id="5d943-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d943-192">8</span><span class="sxs-lookup"><span data-stu-id="5d943-192">8</span></span></td>
<td><span data-ttu-id="5d943-193">Dispositivo seriale</span><span class="sxs-lookup"><span data-stu-id="5d943-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d943-194">16</span><span class="sxs-lookup"><span data-stu-id="5d943-194">16</span></span></td>
<td><span data-ttu-id="5d943-195">Dispositivo parallelo</span><span class="sxs-lookup"><span data-stu-id="5d943-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="5d943-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-197">Impostazione della velocità in baud corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="5d943-198">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-199">&quot; &quot; Se il dispositivo non è connesso da un cavo seriale, il valore deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="5d943-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="5d943-200">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="5d943-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-202">Funzionalità di STI generiche per il dispositivo ottenute dal file INF.</span><span class="sxs-lookup"><span data-stu-id="5d943-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="5d943-203">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-204">Un'applicazione legge questa proprietà per determinare le funzionalità di STI generiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="5d943-205">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="5d943-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-207">Numero (sotto forma di stringa) della versione WIA corrente installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5d943-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="5d943-208">Un'applicazione legge questa proprietà per determinare la versione di WIA installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5d943-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="5d943-209">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-210">Questa proprietà è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5d943-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="5d943-211">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="5d943-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-213">Versione della DLL corrente del minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="5d943-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="5d943-214">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-215">Questa proprietà è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5d943-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="5d943-216">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="5d943-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-218">ID PnP corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d943-218">The current PnP id for the device.</span></span> <span data-ttu-id="5d943-219">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-220">Questa proprietà è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5d943-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="5d943-221">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="5d943-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="5d943-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="5d943-223">Versione generica del driver STI.</span><span class="sxs-lookup"><span data-stu-id="5d943-223">The generic STI driver version.</span></span> <span data-ttu-id="5d943-224">Il servizio WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d943-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="5d943-225">Un'applicazione legge questa proprietà per determinare la versione generica del driver STI.</span><span class="sxs-lookup"><span data-stu-id="5d943-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="5d943-226">Questa proprietà è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5d943-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="5d943-227">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="5d943-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="5d943-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d943-228">Requirements</span></span>



| <span data-ttu-id="5d943-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d943-229">Requirement</span></span> | <span data-ttu-id="5d943-230">Valore</span><span class="sxs-lookup"><span data-stu-id="5d943-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d943-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d943-231">Minimum supported client</span></span><br/> | <span data-ttu-id="5d943-232">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d943-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5d943-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d943-233">Minimum supported server</span></span><br/> | <span data-ttu-id="5d943-234">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d943-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d943-235">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d943-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d943-236"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d943-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




