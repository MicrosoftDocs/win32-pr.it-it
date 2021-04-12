---
title: Servizi Desktop remoto codici di errore del provider WMI (Wbemcli. h)
description: Errori restituiti dal provider WMI Servizi Desktop remoto. Per un elenco di altri errori WMI, vedere costanti di errore WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518988"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>Servizi Desktop remoto codici di errore del provider WMI

Nell'elenco seguente sono elencati gli errori WMI restituiti dal provider WMI Servizi Desktop remoto. Per un elenco di altri errori WMI, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ non riuscito**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



La chiamata al metodo non è riuscita.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Impossibile trovare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_errore del \_ provider WBEM E \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Il provider ha avuto esito negativo in un momento diverso dall'inizializzazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_tipo WBEM E non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Si è verificata una mancata corrispondenza del tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ \_ \_ memoria insufficiente**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Memoria insufficiente per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_parametro WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Uno dei parametri della chiamata non è corretto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



La risorsa, tipicamente un server remoto, non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ supportato**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



La funzionalità o l'operazione non è supportata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_ \_ spazio dei nomi WBEM E non valido \_**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



Impossibile trovare lo spazio dei nomi specificato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_oggetto WBEM E \_ non valido \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



L'istanza specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_errore di \_ inizializzazione WBEM E \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Non è stato possibile inizializzare un modulo, ad esempio un provider, per motivi interni.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_operazione WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Il tipo di operazione richiesta non è valido. Questo errore si applica generalmente a tentativi non validi di eliminare classi o proprietà. Questo errore viene restituito quando si tenta di modificare una proprietà di sostituzione del server tramite il controllo criteri di gruppo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_query WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La sintassi della query non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo di query WBEM E \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Il linguaggio della query richiesta non è supportato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ esiste già**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



In un'operazione Put è stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_sintassi WBEM E \_ non valida \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La query non è sintatticamente valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ sola lettura \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



La proprietà che si tenta di modificare è di sola lettura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**il \_ provider WBEM E \_ \_ non è \_ in grado di supportare**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Il provider non è in grado di eseguire l'operazione richiesta. L'operazione potrebbe includere una query troppo complessa, il recupero di un'istanza, la creazione di una classe, l'aggiornamento di una classe, l'eliminazione di una classe o l'enumerazione di una classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non valido \_**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Non è stato specificato **alcun** valore / **null** per una proprietà che non può essere  / **null**, ad esempio una chiave contrassegnata da un qualificatore di [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**indicizzato**](/windows/desktop/WmiSdk/optional-qualifiers)o [**Not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valore WBEM E non compreso nell' \_ \_ \_ \_ intervallo**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La richiesta è stata eseguita con un valore esterno all'intervallo o è incompatibile con il tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ metodo non valido \_**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



Il metodo richiesto non è disponibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parametri del metodo WBEM E \_ non validi \_ \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



I parametri forniti per il metodo non sono validi.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_percorso dell'oggetto WBEM E \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Il percorso dell'oggetto specificato non è valido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



 

