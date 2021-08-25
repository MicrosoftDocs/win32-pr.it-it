---
title: Servizi Desktop remoto di errore del provider WMI (Wbemcli.h)
description: Errori restituiti dal Servizi Desktop remoto WMI. Per un elenco di altri errori WMI, vedere Costanti di errore WMI.
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
ms.openlocfilehash: f02b2c1cc07bbe9431f2d0e64252258d76de9e6f06c0d7b756b3a5af4e42bff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869671"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>Servizi Desktop remoto di errore del provider WMI

Nell'elenco seguente sono elencati gli errori WMI restituiti dal Servizi Desktop remoto WMI. Per un elenco di altri errori WMI, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



La chiamata al metodo non è riuscita.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Impossibile trovare l'oggetto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**ERRORE DEL \_ PROVIDER WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Il provider ha avuto esito negativo in un momento diverso da durante l'inizializzazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**MANCATA \_ CORRISPONDENZA DEL TIPO E \_ WBEM \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Si è verificata una mancata corrispondenza del tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**MEMORIA INSUFFICIENTE PER WBEM \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Memoria insufficiente per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**PARAMETRO WBEM \_ E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Uno dei parametri della chiamata non è corretto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ NON \_ DISPONIBILE**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



La risorsa, tipicamente un server remoto, non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



La funzionalità o l'operazione non è supportata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**SPAZIO DEI NOMI WBEM \_ E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



Impossibile trovare lo spazio dei nomi specificato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**OGGETTO WBEM \_ E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



L'istanza specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**ERRORE DI \_ INIZIALIZZAZIONE WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Un modulo, ad esempio un provider, non è stato inizializzato per motivi interni.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**OPERAZIONE WBEM \_ E \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Il tipo di operazione richiesta non è valido. Questo errore si applica generalmente a tentativi non validi di eliminare classi o proprietà. Questo errore viene restituito nel tentativo di modificare una proprietà di override del server tramite il controllo Criteri di gruppo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**QUERY WBEM \_ E \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La sintassi della query non è valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**TIPO DI QUERY WBEM \_ E \_ NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Il linguaggio della query richiesta non è supportato.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ ESISTE \_ GIÀ**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



In un'operazione put è stato specificato il flag **wbemChangeFlagCreateOnly,** ma l'istanza esiste già.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**SINTASSI WBEM \_ E \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La query non è sintatticamente valida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E DI SOLA \_ \_ LETTURA**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



La proprietà che si tenta di modificare è di sola lettura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**PROVIDER WBEM \_ E \_ NON \_ \_ IDONEO**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Il provider non può eseguire l'operazione richiesta. L'operazione può includere una query troppo complessa, il recupero di un'istanza, la creazione di una classe, l'aggiornamento di una classe, l'eliminazione di una classe o l'enumerazione di una classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E NULL NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



È stato specificato **un valore Nothing** NULL per una proprietà che non può essere Nothing NULL, ad esempio uno contrassegnato da un qualificatore /   /  [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Indexed**](/windows/desktop/WmiSdk/optional-qualifiers)o [**Not \_ Null.**](/windows/desktop/WmiSdk/optional-qualifiers)


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**VALORE \_ WBEM E NON COMPRESO \_ \_ \_ \_ NELL'INTERVALLO**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La richiesta è stata eseguita con un valore esterno all'intervallo o è incompatibile con il tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**METODO WBEM \_ E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



Il metodo richiesto non è disponibile.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**PARAMETRI DEL METODO \_ WBEM E \_ NON \_ \_ VALIDI**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



I parametri forniti per il metodo non sono validi.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**PERCORSO \_ DELL'OGGETTO WBEM E NON \_ \_ \_ VALIDO**
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
| Intestazione<br/>                   | <dl> <dt>Wbemcli.h</dt> </dl> |



 

