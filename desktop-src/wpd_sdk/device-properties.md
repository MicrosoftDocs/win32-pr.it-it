---
description: Dispositivi portatili Windows supporta le seguenti proprietà del dispositivo.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Proprietà del dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328972"
---
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="785e9-103">Proprietà del dispositivo (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="785e9-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="785e9-104">Dispositivi portatili Windows supporta le seguenti proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="785e9-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="785e9-105">Property</span></span></th>
<th><span data-ttu-id="785e9-106">VarType</span><span class="sxs-lookup"><span data-stu-id="785e9-106">VarType</span></span></th>
<th><span data-ttu-id="785e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="785e9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="785e9-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="785e9-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="785e9-110">Data e ora correnti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="785e9-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-113">Versione del firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="785e9-115"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="785e9-116">Identificatore univoco a 16 byte comune tra più trasporti supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="785e9-117">Se un singolo dispositivo supporta più trasporti, questa proprietà può essere usata per associare i vari driver WPD di trasporto a tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="785e9-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-120">Nome del produttore di dispositivi leggibile.</span><span class="sxs-lookup"><span data-stu-id="785e9-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="785e9-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-123">Modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="785e9-125"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="785e9-126">Identificatore univoco a 16 byte usato per distinguere tra modelli diversi di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="785e9-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="785e9-129">Valore che specifica l'identificatore di rete EUI-64 del dispositivo. Questa proprietà viene utilizzata per le operazioni di rete fuori banda. Se il dispositivo dispone di indirizzi di rete fisica MAC-48 (tipici di reti IPv4), l'indirizzo MAC-48 viene codificato nell'indirizzo EUI-64 come due metà dell'indirizzo MAC-48 separato da FF-FF.</span><span class="sxs-lookup"><span data-stu-id="785e9-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="785e9-130">Il valore EUI-64 viene archiviato in &quot; ordine di rete &quot; o &quot; Big-Endian &quot; , in cui un indirizzo EUI-64 01-02-03-FF-FF-04-05-06 viene inserito nella VT_UI8 in modo che il valore decimale sia 72624942021346566.</span><span class="sxs-lookup"><span data-stu-id="785e9-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="785e9-131">Questa proprietà è obbligatoria per tutti i dispositivi che supportano l'autenticazione nominale o protetta.</span><span class="sxs-lookup"><span data-stu-id="785e9-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="785e9-132">Questa proprietà è consigliata nei dispositivi che supportano solo l'autenticazione zero.</span><span class="sxs-lookup"><span data-stu-id="785e9-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="785e9-133">Il valore può essere usato dall'host per stabilire automaticamente l'accesso al dispositivo senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="785e9-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="785e9-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="785e9-136">Valore compreso tra 0 e 100 che specifica il livello di alimentazione della batteria del dispositivo, con 0 come None e 100 completamente addebitato.</span><span class="sxs-lookup"><span data-stu-id="785e9-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="785e9-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="785e9-138">VT_UI4</span></span></td>
<td><span data-ttu-id="785e9-139">Enumerazione <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> che specifica la fonte di alimentazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="785e9-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-142">Protocollo del dispositivo in uso.</span><span class="sxs-lookup"><span data-stu-id="785e9-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="785e9-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-145">Numero di serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="785e9-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="785e9-148">Valore che specifica se i formati supportati restituiti dal dispositivo sono in un ordine preferenziale.</span><span class="sxs-lookup"><span data-stu-id="785e9-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="785e9-149">Il primo formato dell'elenco è preferito dal dispositivo, mentre l'ultimo è il meno preferibile. Le applicazioni possono usare questa proprietà per determinare se i formati supportati da un dispositivo sono elencati in un ordine preferito.</span><span class="sxs-lookup"><span data-stu-id="785e9-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="785e9-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="785e9-152">Valore booleano che specifica se i formati supportati restituiti dal dispositivo sono in un ordine preferito; ovvero, è preferibile il primo formato restituito, mentre l'ultimo formato restituito è il meno preferibile.</span><span class="sxs-lookup"><span data-stu-id="785e9-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="785e9-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="785e9-155">Valore booleano che specifica se il dispositivo supporta oggetti non utilizzabili.</span><span class="sxs-lookup"><span data-stu-id="785e9-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="785e9-156">Si tratta di oggetti che il dispositivo è destinato solo a archiviare, non riprodurre o utilizzare in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="785e9-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="785e9-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-159">Descrizione leggibile del <em>partner di sincronizzazione</em>di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="785e9-160">Si tratta di un dispositivo, un'applicazione o un server con il quale comunica il dispositivo per mantenere uno stato comune o un gruppo di file tra entrambi i partner.</span><span class="sxs-lookup"><span data-stu-id="785e9-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="785e9-161">Gli esempi includono programmi di posta elettronica e librerie di musica.</span><span class="sxs-lookup"><span data-stu-id="785e9-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="785e9-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="785e9-164">Valore che rappresenta il nome descrittivo impostato dall'utente sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="785e9-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="785e9-167">il trasporto supportato dal dispositivo, ad esempio USB, IP o Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="785e9-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="785e9-168">I valori validi sono del tipo di enumerazione <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="785e9-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="785e9-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="785e9-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="785e9-171">Valore che specifica il tipo di dispositivo; le applicazioni utilizzano questa proprietà solo a scopo di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="785e9-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="785e9-172">Le caratteristiche funzionali del dispositivo vengono decise tramite oggetti funzionali. I dispositivi che non forniscono un'icona di dispositivo, ad esempio un <strong>WPD_RESOURCE_ICON</strong> per l'oggetto dispositivo, verranno rappresentati nello spazio dei nomi WPD con un'icona generica.</span><span class="sxs-lookup"><span data-stu-id="785e9-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="785e9-173">Questa icona dipenderà dal tipo di dispositivo specificato. ad esempio, se il tipo di dispositivo è un telefono cellulare, viene utilizzata l'icona generica Phone.</span><span class="sxs-lookup"><span data-stu-id="785e9-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="785e9-174">Alla prima installazione del dispositivo, il programma di installazione della classe WPD eseguirà una query sul valore della proprietà e lo archivia nel registro di sistema del dispositivo sotto il valore PORTABLE_DEVICE_TYPE come REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="785e9-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="785e9-175">I valori possibili di questo parametro sono delineati dall'enumerazione <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> definita in portabledevice. h.</span><span class="sxs-lookup"><span data-stu-id="785e9-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="785e9-176">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="785e9-176">Values are:</span></span><br/> <dl> <span data-ttu-id="785e9-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="785e9-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="785e9-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="785e9-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="785e9-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="785e9-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="785e9-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="785e9-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="785e9-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="785e9-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="785e9-186">Se questa proprietà esiste ed è impostata su <strong>true</strong>, il dispositivo può essere usato con la fase del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785e9-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="785e9-187">Questa operazione è destinata ai dispositivi che non possono archiviare i metadati usando il <strong>servizio metadati del dispositivo</strong>, ma forniranno metadati sui server Microsoft.</span><span class="sxs-lookup"><span data-stu-id="785e9-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="785e9-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="785e9-188">Requirements</span></span>



| <span data-ttu-id="785e9-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="785e9-189">Requirement</span></span> | <span data-ttu-id="785e9-190">Valore</span><span class="sxs-lookup"><span data-stu-id="785e9-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="785e9-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="785e9-191">Header</span></span><br/> | <dl> <span data-ttu-id="785e9-192"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="785e9-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="785e9-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="785e9-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785e9-194">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="785e9-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




