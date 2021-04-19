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
# <a name="device-properties-portabledeviceh"></a>Proprietà del dispositivo (PortableDevice. h)

Dispositivi portatili Windows supporta le seguenti proprietà del dispositivo.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>VarType</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>Data e ora correnti del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Versione del firmware del dispositivo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Identificatore univoco a 16 byte comune tra più trasporti supportati dal dispositivo. Se un singolo dispositivo supporta più trasporti, questa proprietà può essere usata per associare i vari driver WPD di trasporto a tale dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Nome del produttore di dispositivi leggibile.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Modello del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Identificatore univoco a 16 byte usato per distinguere tra modelli diversi di un dispositivo.</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>Valore che specifica l'identificatore di rete EUI-64 del dispositivo. Questa proprietà viene utilizzata per le operazioni di rete fuori banda. Se il dispositivo dispone di indirizzi di rete fisica MAC-48 (tipici di reti IPv4), l'indirizzo MAC-48 viene codificato nell'indirizzo EUI-64 come due metà dell'indirizzo MAC-48 separato da FF-FF. Il valore EUI-64 viene archiviato in &quot; ordine di rete &quot; o &quot; Big-Endian &quot; , in cui un indirizzo EUI-64 01-02-03-FF-FF-04-05-06 viene inserito nella VT_UI8 in modo che il valore decimale sia 72624942021346566. Questa proprietà è obbligatoria per tutti i dispositivi che supportano l'autenticazione nominale o protetta. Questa proprietà è consigliata nei dispositivi che supportano solo l'autenticazione zero. Il valore può essere usato dall'host per stabilire automaticamente l'accesso al dispositivo senza l'intervento dell'utente.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valore compreso tra 0 e 100 che specifica il livello di alimentazione della batteria del dispositivo, con 0 come None e 100 completamente addebitato.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Enumerazione <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> che specifica la fonte di alimentazione del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Protocollo del dispositivo in uso.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Numero di serie del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Valore che specifica se i formati supportati restituiti dal dispositivo sono in un ordine preferenziale. Il primo formato dell'elenco è preferito dal dispositivo, mentre l'ultimo è il meno preferibile. Le applicazioni possono usare questa proprietà per determinare se i formati supportati da un dispositivo sono elencati in un ordine preferito.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valore booleano che specifica se i formati supportati restituiti dal dispositivo sono in un ordine preferito; ovvero, è preferibile il primo formato restituito, mentre l'ultimo formato restituito è il meno preferibile.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valore booleano che specifica se il dispositivo supporta oggetti non utilizzabili. Si tratta di oggetti che il dispositivo è destinato solo a archiviare, non riprodurre o utilizzare in alcun modo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Descrizione leggibile del <em>partner di sincronizzazione</em>di un dispositivo. Si tratta di un dispositivo, un'applicazione o un server con il quale comunica il dispositivo per mantenere uno stato comune o un gruppo di file tra entrambi i partner. Gli esempi includono programmi di posta elettronica e librerie di musica.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valore che rappresenta il nome descrittivo impostato dall'utente sul dispositivo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>il trasporto supportato dal dispositivo, ad esempio USB, IP o Bluetooth. I valori validi sono del tipo di enumerazione <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valore che specifica il tipo di dispositivo; le applicazioni utilizzano questa proprietà solo a scopo di rappresentazione. Le caratteristiche funzionali del dispositivo vengono decise tramite oggetti funzionali. I dispositivi che non forniscono un'icona di dispositivo, ad esempio un <strong>WPD_RESOURCE_ICON</strong> per l'oggetto dispositivo, verranno rappresentati nello spazio dei nomi WPD con un'icona generica. Questa icona dipenderà dal tipo di dispositivo specificato. ad esempio, se il tipo di dispositivo è un telefono cellulare, viene utilizzata l'icona generica Phone. Alla prima installazione del dispositivo, il programma di installazione della classe WPD eseguirà una query sul valore della proprietà e lo archivia nel registro di sistema del dispositivo sotto il valore PORTABLE_DEVICE_TYPE come REG_DWORD.<br/> I valori possibili di questo parametro sono delineati dall'enumerazione <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> definita in portabledevice. h. I valori possibili sono:<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Se questa proprietà esiste ed è impostata su <strong>true</strong>, il dispositivo può essere usato con la fase del dispositivo. Questa operazione è destinata ai dispositivi che non possono archiviare i metadati usando il <strong>servizio metadati del dispositivo</strong>, ma forniranno metadati sui server Microsoft.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




