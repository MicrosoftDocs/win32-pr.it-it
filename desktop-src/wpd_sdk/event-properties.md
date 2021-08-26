---
description: Windows Dispositivi portabili supporta le proprietà degli eventi seguenti.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Proprietà evento (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f5220b7cd3b0acfb70788a62138a7da3a4ebac008a51e90bbc93308ae2624300
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055351"
---
# <a name="event-properties"></a>Proprietà dell'evento

Windows Dispositivi portabili supporta le proprietà degli eventi seguenti.



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
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Riservato per utilizzi futuri.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valore booleano che specifica se l'evento viene trasmesso a tutti i client. I client possono ricevere questo evento registrando il callback con <strong>IPortableDevice::Advise.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valore booleano che specifica se la gerarchia figlio per l'oggetto è stata modificata. Questo parametro viene utilizzato per notificare al chiamante che alcuni elementi figlio per l'oggetto specificato sono stati aggiunti o rimossi. In genere la modifica della gerarchia viene avviata sul lato dispositivo. Potrebbe essere necessario enumerare nuovamente gli elementi figlio di questa cartella per mantenere aggiornate le visualizzazioni.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Valore che identifica un evento.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Il cookie restituito a un client quando richiede la creazione di un oggetto chiamando il <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>metodo IPortableDeviceContent::CreateObjectWithPropertiesAndData.</strong></a> Questo parametro viene aggiunto per comodità per consentire al chiamante di associare un evento aggiunto all'oggetto alla richiesta inviata per creare l'oggetto. Il driver restituisce questo cookie come valore <strong>restituito WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> durante l'elaborazione <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> comando.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valore che identifica in modo univoco l'oggetto padre. Questa proprietà è simile a <strong>WPD_OBJECT_PARENT_ID</strong>, ma questo ID non cambia da una sessione all'altra.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valore che specifica lo stato di avanzamento di un'operazione attualmente in esecuzione. Il valore di questa proprietà può essere compreso tra 0 e 100, con 100 che indica che l'operazione è stata completata.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valore che indica lo stato corrente dell'operazione, ad esempio avviato, in esecuzione, arrestato e così via. I valori possibili di questo parametro derivano <strong>dall'WPD_OPERATION_STATES</strong> definita in PortableDevice.h. I valori possibili sono:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valore che specifica il dispositivo che ha originato l'evento. Si tratta dell'identificatore del dispositivo o del servizio fornito dal sistema Plug-and-Play (PnP) ed è la stessa stringa usata nei metodi <strong>IPortableDevice::Open</strong>o <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open.</strong></a><br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Stringa usata da un driver WPD per identificare il funzionamento di un metodo device-service. Le applicazioni non devono usare direttamente questo parametro.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




