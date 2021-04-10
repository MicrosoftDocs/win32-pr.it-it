---
title: Costanti di errore NAP (WinError. h)
description: Le costanti di errore NAP seguenti sono definite in WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964716"
---
# <a name="nap-error-constants"></a>Costanti di errore NAP

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Le costanti di errore NAP seguenti sono definite in WinError. h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP \_ E \_ pacchetto non valido \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270001L)
</dt> <dt>



Il pacchetto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) NAP non è valido.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E rapporto di \_ \_ integrità mancante**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270002L)
</dt> <dt>



Nel pacchetto NAP manca un rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**protezione accesso alla rete \_ E \_ ID in conflitto \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270003L)
</dt> <dt>



L'ID entità è in conflitto con un ID entità già registrato.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ nessun rapporto di \_ integrità memorizzato nella cache \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270004L)
</dt> <dt>



Non è presente alcun rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) memorizzato nella cache.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ ancora \_ associato**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270005L)
</dt> <dt>



L'entità è ancora associata al sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ non \_ registrato**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270006L)
</dt> <dt>



L'entità non è registrata nel sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ non \_ inizializzato**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270007L)
</dt> <dt>



L'entità non è inizializzata con il sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**\_ID NAP E non \_ corrispondente \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270008L)
</dt> <dt>



Gli ID di correlazione nella **richiesta e nella** risposta di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) non corrispondono.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ non \_ in sospeso**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270009L)
</dt> <dt>



Il completamento è stato indicato in una richiesta che non è attualmente in sospeso.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**NAP \_ E \_ ID \_ non \_ trovati**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x8027000AL)
</dt> <dt>



ID del componente NAP non trovato.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MaxSize \_ troppo \_ piccoli**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x8027000BL)
</dt> <dt>



La dimensione massima della connessione è troppo piccola per un pacchetto di rapporto di integrità.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**\_servizio NAP \_ E \_ non \_ in esecuzione**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x8027000CL)
</dt> <dt>



Il servizio NapAgent non è in esecuzione.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**il \_ certificato NAP S è \_ \_ già \_ presente**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x0027000DL) 
</dt> <dt>



Un certificato è già presente nell'archivio certificati.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**protezione accesso alla rete \_ E \_ entità \_ disabilitata**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x8027000EL)
</dt> <dt>



L'entità è disabilitata con il servizio NapAgent.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**errore di protezione accesso alla rete \_ E \_ netsh \_ GROUPPOLICY \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x8027000FL)
</dt> <dt>



Criteri di gruppo non è configurato.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ numero eccessivo di \_ \_ chiamate**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270010L)
</dt> <dt>



Troppe chiamate simultanee.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ esistente**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270011L)
</dt> <dt>



La configurazione di convalida integrità sistema esiste già.

> [!Note]  
> Supportato in Windows 7 o versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270012L)
</dt> <dt>



Configurazione di convalida integrità sistema non trovata.

> [!Note]  
> Supportato in Windows 7 o versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**TIMEOUT di protezione accesso alla rete \_ E di \_ integrità \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (0x80270013L)
</dt> <dt>



Timeout di convalida integrità di sistema nella richiesta.

> [!Note]  
> Supportato in Windows 7 o versioni successive.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti NAP**](nap-constants.md)
</dt> </dl>

 

 





