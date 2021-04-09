---
description: Sono incluse informazioni sulla gravità, la cause, le azioni consigliate e altri dati correlati all'esito negativo di un'operazione CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Classe Msvm_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050085"
---
# <a name="msvm_error-class"></a>\_Classe di errore MSVM

Classe specializzata che contiene informazioni sulla gravità, la cause, le azioni consigliate e altri dati correlati all'esito negativo di un'operazione CIM.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a>Members

La classe di **\_ errore MSVM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ errore MSVM** dispone di queste proprietà.

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Codice di stato CIM che caratterizza questa istanza. Questa proprietà definisce i codici di stato che possono essere restituiti da un listener o un server CIM conforme. Non tutti i codici di stato sono validi per ogni operazione. La specifica per ogni operazione deve definire i codici di stato che possono essere restituiti da tale operazione. Sono definiti i valori seguenti per il codice di stato CIM. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).



| Valore                                                                                                                                                                                                                                                                                          | Significato                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <dt>**CIM \_ ERRORE \_**</dt> <dt>1</dt> </dl>                                                                       | Si è verificato un errore generale che non è coperto da un codice di errore più specifico.<br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <dt>**CIM \_ ERRORE di \_ accesso \_ negato**</dt> <dt>2</dt> </dl>                                                 | L'accesso a una risorsa CIM non è disponibile per il client.<br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <dt>**CIM \_ ERRORE \_ \_ spazio dei nomi**</dt> <dt>3</dt> errato </dl>                                     | Lo spazio dei nomi di destinazione non esiste.<br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <dt>**CIM \_ ERR \_ \_ parametro 4 non valido**</dt> <dt></dt> </dl>                                     | Uno o più valori di parametro passati al metodo non sono validi.<br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <dt>**CIM \_ ERR \_ \_ classe 5 non valida**</dt> <dt></dt> </dl>                                                 | La classe specificata non esiste.<br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <dt>**CIM \_ ERRORE \_ non \_ trovato**</dt> <dt>6</dt> </dl>                                                             | Impossibile trovare l'oggetto richiesto.<br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <dt>**CIM \_ ERR \_ non \_ supportato**</dt> <dt>7</dt> </dl>                                                 | L'operazione richiesta non è supportata.<br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <dt>**CIM \_ \_Classe ERR \_ con \_ figli**</dt> <dt>8</dt> </dl>                                 | Non è possibile eseguire l'operazione su questa classe perché contiene istanze.<br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <dt>**CIM \_ \_Classe ERR \_ con \_ istanze**</dt> <dt>9</dt> </dl>                              | Non è possibile eseguire l'operazione su questa classe perché contiene istanze.<br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <dt>**CIM \_ ERRORE \_ \_ superclasse**</dt> <dt>10</dt> </dl>                                 | Non è possibile eseguire l'operazione perché la superclasse specificata non esiste.<br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <dt>**CIM \_ Il \_ Err \_ esiste già**</dt> <dt>11</dt> </dl>                                             | Non è possibile eseguire l'operazione perché esiste già un oggetto.<br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <dt>**CIM \_ \_Nessuna \_ \_ proprietà di questo tipo**</dt> <dt>12</dt> </dl>                                      | La proprietà specificata non esiste.<br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <dt>**CIM \_ Tipo ERR non \_ \_ corrispondente**</dt> <dt>13</dt> </dl>                                                | Il valore specificato non è compatibile con il tipo.<br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <dt>**CIM \_ Il \_ linguaggio di query ERR \_ non è \_ \_ supportato**</dt> <dt>14</dt> </dl> | Il linguaggio di query non è riconosciuto né supportato.<br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <dt>**CIM \_ \_ \_ Query Err non valida**</dt> <dt>15</dt> </dl>                                                | La query non è valida per il linguaggio di query specificato.<br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <dt>**CIM \_ \_Metodo ERR \_ non \_ disponibile**</dt> <dt>16</dt> </dl>                          | Impossibile eseguire il metodo estrinseco.<br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <dt>**CIM \_ \_Metodo ERR \_ non \_ trovato**</dt> <dt>17</dt> </dl>                                      | Il metodo estrinseco specificato non esiste.<br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <dt>**CIM \_ \_ \_ Risposta imprevista a Err**</dt> <dt>18</dt> </dl>                              | La risposta restituita all'operazione asincrona non era prevista.<br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <dt>**CIM \_ ERRORE \_ \_ \_ destinazione risposta non valida**</dt> <dt>19</dt> </dl>  | La destinazione specificata per la risposta asincrona non è valida.<br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <dt>**CIM \_ \_Spazio dei nomi ERR \_ non \_ vuoto**</dt> <dt>20</dt> </dl>                             | Lo spazio dei nomi specificato non è vuoto.<br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt>**DMTF riservato**</dt> <dt>21 = *valore*</dt> </dl>                            | Valori riservati.<br/>                                                               |



 

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa contenente una descrizione leggibile dall'utente della proprietà **CIMStatusCode** . Questa descrizione può estendersi, ma deve essere coerente con la definizione di **CIMStatusCode**. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni di identificazione dell'entità, ovvero l'istanza, che genera l'errore. Se questa entità è modellata nello schema CIM, questa proprietà contiene il percorso dell'istanza codificata come parametro di stringa. Se non è modellato, la proprietà contiene una stringa di identificazione che assegna un nome all'entità che ha generato l'errore. Il percorso o la stringa di identificazione viene formattato in base alla proprietà **ErrorSourceFormat** . Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il formato della proprietà **ErrorSource** è interpretabile in base al valore di questa proprietà. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85))ed è sempre impostata su 0.



| Valore                                                                                                                                                                                                                                                        | Significato                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                  | Il formato è sconosciuto o non interpretabile in maniera significativa da un'applicazione client CIM.<br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                          | Il formato è definito dal valore della proprietà **OtherErrorSourceFormat** .<br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <dt>**CIMObjectHandle**</dt> <dt>2</dt> </dl> | Per identificare l'entità, viene usato un handle di oggetto CIM, codificato usando la sintassi MOF definita per objectHandle non terminale.<br/> |



 

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Classificazione primaria dell'errore. Vengono definiti i valori seguenti. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).



| Valore                                                                                                                                                                                                                                                                                                         | Significato                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <dt>**Errore di comunicazione**</dt> <dt>2</dt> </dl>                               | Gli errori di questo tipo sono associati principalmente alle procedure e/o ai processi necessari per il trasferimento di informazioni da un punto a un altro.<br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <dt>**Qualità del servizio-errore**</dt> <dt>3</dt> </dl>               | Gli errori di questo tipo sono associati principalmente a errori che comportano una riduzione delle prestazioni o delle funzionalità.<br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <dt>**Errore software**</dt> <dt>4</dt> </dl>                                                       | Un errore di questo tipo è associato principalmente a un errore software o di elaborazione.<br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <dt>**Errore hardware**</dt> <dt>5</dt> </dl>                                                       | Gli errori di questo tipo sono associati principalmente a un errore hardware o di apparecchiature.<br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <dt>**Errore ambientale**</dt> <dt>6</dt> </dl>                                   | Gli errori di questo tipo sono associati principalmente a una condizione di errore relativa alla struttura o ad altre considerazioni sull'ambiente.<br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <dt>**Errore di sicurezza**</dt> <dt>7</dt> </dl>                                                       | Gli errori di questo tipo sono associati a violazioni di sicurezza, rilevamento di virus e problemi simili.<br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <dt>**Errore oversubscription**</dt> <dt>8</dt> </dl>                       | Gli errori di questo tipo sono associati principalmente all'esito negativo di allocare risorse sufficienti per completare l'operazione.<br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <dt>**Errore di risorsa non disponibile**</dt> <dt>9</dt> </dl>       | Gli errori di questo tipo sono associati principalmente all'esito negativo dell'accesso a una risorsa necessaria.<br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <dt>**Errore di operazione**</dt> <dt>10</dt> non supportato </dl> | Gli errori di questo tipo sono associati principalmente a richieste non supportate.<br/>                                                          |



 

</dd> <dt>

**Messaggio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Messaggio formattato. Questo messaggio viene costruito applicando il contenuto dinamico del messaggio, descritto in **MessageArguments**, alla stringa di formato identificata in modo univoco, all'interno dell'ambito di **OwningEntity**, da **MessageID**. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice contenente il contenuto dinamico del messaggio. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa opaca che identifica in modo univoco, all'interno dell'ambito di **OwningEntity**, il formato del messaggio. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che definisce i valori "other" per **ErrorSourceFormat**. Questo valore deve essere impostato su un valore non NULL quando **ErrorSourceFormat** è impostato su un valore di 1 (other). Per tutti gli altri valori di **ErrorSourceFormat**, il valore di questa stringa deve essere impostato su **null**. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive **ErrorType** quando 1, (other), viene specificato come **ErrorType**. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che identifica in modo univoco l'entità a cui appartiene la definizione del formato del messaggio descritto in questa istanza. **OwningEntity** deve includere un nome con copyright, marchio o in altro modo univoco di proprietà dell'entità di business o del corpo degli standard che definisce il formato. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore enumerato che descrive la gravità dell'errore dal punto di vista del notificatore: 2-basso deve essere usato per problemi non critici, ad esempio parametri non validi, utilizzo errato, funzionalità non supportate. 3-medium deve essere usato per indicare che l'azione è necessaria, ma in questo momento la situazione non è grave. 4-High deve essere usato per indicare che l'azione è ora necessaria. 5: è consigliabile usare un valore irreversibile per indicare una perdita di dati o un errore irreversibile del sistema o del servizio. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (2)
</dt> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Media** (3)
</dt> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (4)
</dt> <dt>

<span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Irreversibile** (5)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore enumerato che descrive la probabile cause dell'errore. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Errore scheda/scheda** (2)
</dt> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Errore del sottosistema dell'applicazione** (3)
</dt> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Larghezza di banda ridotta** (4)
</dt> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Errore di creazione connessione** (5)
</dt> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Errore del protocollo di comunicazione** (6)
</dt> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Errore del sottosistema di comunicazione** (7)
</dt> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Errore di configurazione/personalizzazione** (8)
</dt> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestione** (9)
</dt> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Dati danneggiati** (10)
</dt> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Limite cicli CPU superato** (11)
</dt> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Errore del set di dati/modem** (12)
</dt> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Segnale danneggiato** (13)
</dt> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**Errore di interfaccia DTE-DCE** (14)
</dt> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Sportello enclosure aperto** (15)
</dt> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Malfunzionamento delle apparecchiature** (16)
</dt> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Vibrazione eccessiva** (17)
</dt> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Errore di formato del file** (18)
</dt> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire detected** (19)
</dt> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood rilevato** (20)
</dt> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Errore di framing** (21)
</dt> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Problema HVAC** (22)
</dt> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Umidità inaccettabile** (23)
</dt> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Errore del dispositivo di I/O** (24)
</dt> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Errore dispositivo di input** (25)
</dt> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Errore LAN** (26)
</dt> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>È stata **rilevata una perdita non tossica** (27)
</dt> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Errore di trasmissione del nodo locale** (28)
</dt> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Perdita di frame** (29)
</dt> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Perdita del segnale** (30)
</dt> <dt>

<span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 approvvigionamento materiale esaurito** (31)
</dt> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Problema del multiplexer** (32)
</dt> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Memoria insufficiente** (33)
</dt> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Errore dispositivo di output** (34)
</dt> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Prestazioni** ridotte (35)
</dt> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Problema di alimentazione** (36)
</dt> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressione inaccettabile** (37)
</dt> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Problema del processore (errore interno del computer)** (38)
</dt> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Errore della pompa** (39)
</dt> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Dimensione coda superata** (40)
</dt> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Errore di ricezione** (41)
</dt> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Errore del ricevitore** (42)
</dt> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Errore di trasmissione del nodo remoto** (43)
</dt> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Risorsa alla capacità o al prossimo livello** (44)
</dt> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Tempo di risposta eccessivo** (45)
</dt> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Frequenza di ritrasmissione eccessiva** (46)
</dt> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Errore software** (47)
</dt> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Programma software terminato in modo anomalo** (48)
</dt> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Errore del programma software (risultati non corretti)** (49)
</dt> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema di capacità di archiviazione** (50)
</dt> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatura inaccettabile** (51)
</dt> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Soglia superata** (52)
</dt> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Problema di temporizzazione** (53)
</dt> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>È stata **rilevata una perdita tossica** (54)
</dt> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Errore di trasmissione** (55)
</dt> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Errore della trasmittente** (56)
</dt> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Risorsa sottostante non disponibile** (57)
</dt> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Versione non corrispondente** (58)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Avviso precedente cancellato** (59)
</dt> <dt>

<span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60 tentativi di accesso non riusciti** (60)
</dt> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Rilevato virus software** (61)
</dt> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Protezione hardware violata** (62)
</dt> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Rilevato un attacco Denial of Service** (63)
</dt> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Mancata corrispondenza delle credenziali di sicurezza** (64)
</dt> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Accesso non autorizzato** (65)
</dt> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Allarme ricevuto** (66)
</dt> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Perdita di puntatore** (67)
</dt> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Mancata corrispondenza del payload** (68)
</dt> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Errore di trasmissione** (69)
</dt> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Frequenza degli errori eccessiva** (70)
</dt> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Problema di traccia** (71)
</dt> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Elemento non disponibile** (72)
</dt> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Elemento mancante** (73)
</dt> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Perdita di più frame** (74)
</dt> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Errore canale broadcast** (75)
</dt> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Ricevuto messaggio non valido** (76)
</dt> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Errore di routing** (77)
</dt> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Errore backplane** (78)
</dt> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Duplicazione degli identificatori** (79)
</dt> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Errore nel percorso di protezione** (80)
</dt> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Perdita di sincronizzazione o mancata corrispondenza** (81)
</dt> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Problema terminale** (82)
</dt> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Errore di clock in tempo reale** (83)
</dt> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Errore antenna** (84)
</dt> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Errore di ricarica della batteria** (85)
</dt> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Errore del disco** (86)
</dt> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Errore di salto della frequenza** (87)
</dt> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Perdita di ridondanza** (88)
</dt> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Errore alimentatore** (89)
</dt> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Problema relativo alla qualità del segnale** (90)
</dt> <dt>

<span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>Scaricamento **batteria 91** (91)
</dt> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Errore batteria** (92)
</dt> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Problema di alimentazione commerciale** (93)
</dt> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Errore ventola** (94)
</dt> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Errore del motore** (95)
</dt> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Errore del sensore** (96)
</dt> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Errore fusibile** (97)
</dt> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Errore del generatore** (98)
</dt> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Batteria insufficiente** (99)
</dt> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Carburante basso** (100)
</dt> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Acqua bassa** (101)
</dt> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gas esplosivo** (102)
</dt> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Venti elevati** (103)
</dt> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Accumulo di ghiaccio** (104)
</dt> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Fumo** (105)
</dt> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memoria non corrispondente** (106)
</dt> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Cicli esauriti CPU** (107)
</dt> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Problema relativo all'ambiente software** (108)
</dt> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Errore di download del software** (109)
</dt> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Elemento reinizializzato** (110)
</dt> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)
</dt> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Problemi di registrazione** (112)
</dt> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Perdita rilevata** (113)
</dt> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Errore del meccanismo di protezione** (114)
</dt> <dt>

<span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**115 protezione errore risorse** (115)
</dt> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Incoerenza del database** (116)
</dt> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Errore di autenticazione** (117)
</dt> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Violazione della riservatezza** (118)
</dt> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Manomissione cavo** (119)
</dt> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Informazioni ritardate** (120)
</dt> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Informazioni duplicate** (121)
</dt> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Informazioni mancanti** (122)
</dt> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Modifica delle informazioni** (123)
</dt> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informazioni fuori sequenza** (124)
</dt> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Chiave scaduta** (125)
</dt> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Errore di non ripudio** (126)
</dt> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Attività fuori orario** (127)
</dt> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Fuori servizio** (128)
</dt> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Errore procedurale** (129)
</dt> <dt>

<span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Informazioni impreviste** (130)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive la probabile cause dell'errore. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive le azioni consigliate da eseguire per risolvere l'errore. Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla classe di **\_ errore MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Errore CIM**](cim-error.md)
</dt> <dt>

[**\_Errore CIM**](/previous-versions//cc150671(v=vs.85))
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

