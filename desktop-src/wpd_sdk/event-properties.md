---
description: I dispositivi portatili Windows supportano le seguenti proprietà dell'evento.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Proprietà evento (PortableDevice. h)
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
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333528"
---
# <a name="event-properties"></a>Proprietà dell'evento

I dispositivi portatili Windows supportano le seguenti proprietà dell'evento.



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
<td>Valore booleano che specifica se l'evento viene trasmesso a tutti i client. I client possono ricevere questo evento registrando il callback con <strong>IPortableDevice:: Advise</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valore booleano che specifica se la gerarchia figlio per l'oggetto è stata modificata. Questo parametro viene utilizzato per notificare al chiamante che alcuni elementi figlio per l'oggetto specificato sono stati aggiunti o rimossi. In genere, la modifica della gerarchia viene avviata sul lato dispositivo. È possibile che i client debbano enumerare di nuovo gli elementi figlio della cartella per mantengono aggiornate le visualizzazioni.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Valore che identifica un evento.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Il cookie viene restituito a un client quando richiede la creazione di un oggetto chiamando il metodo <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent:: CreateObjectWithPropertiesAndData</strong></a> . Questo parametro viene aggiunto come praticità per consentire al chiamante di associare un evento aggiunto a un oggetto alla richiesta inviata per creare l'oggetto. Il driver consegna il cookie come valore restituito <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> durante l'elaborazione del comando di <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valore che identifica in modo univoco l'oggetto padre. Questa proprietà è simile a <strong>WPD_OBJECT_PARENT_ID</strong>, ma questo ID non cambia tra le sessioni.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valore che specifica lo stato di avanzamento di un'operazione attualmente in esecuzione. Il valore di questa proprietà può variare da 0 a 100, con 100 che indica che l'operazione è stata completata.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valore che indica lo stato corrente dell'operazione, ad esempio avviato, in esecuzione, arrestato e così via. I valori possibili di questo parametro sono delineati dall'enumerazione <strong>WPD_OPERATION_STATES</strong> definita in portabledevice. h. I valori possibili sono:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
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
<td>Valore che specifica il dispositivo che ha originato l'evento. Si tratta dell'identificatore del dispositivo o del servizio fornito dal sistema plug-and-Play (PnP) ed è la stessa stringa utilizzata nei metodi <strong>IPortableDevice:: Open</strong>o <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService:: Open</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Stringa utilizzata da un driver WPD per identificare l'operazione di un metodo del servizio del dispositivo. Le applicazioni non devono usare questo parametro direttamente.</td>
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

 

 




