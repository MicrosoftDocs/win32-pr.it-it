---
title: Costanti di errore di Protezione accesso alla rete (WinError.h)
description: Le costanti di errore di Protezione accesso alla rete seguenti sono definite in WinError.h.
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
ms.openlocfilehash: 411500ea5f0fc3ba0f1d4067a6befe902a81af3154c91e76c36425c289616eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620840"
---
# <a name="nap-error-constants"></a>Costanti di errore di Protezione accesso alla rete

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Le costanti di errore di Protezione accesso alla rete seguenti sono definite in WinError.h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**PACCHETTO \_ NON VALIDO DI PROTEZIONE ACCESSO ALLA \_ RETE E \_**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270001L)
</dt> <dt>



Il pacchetto [**SoH di Protezione accesso**](/windows/win32/api/naptypes/ns-naptypes-soh) alla rete non è valido.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**SOH MANCANTE PER PROTEZIONE \_ \_ ACCESSO ALLA \_ RETE**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270002L)
</dt> <dt>



[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) mancante nel pacchetto di Protezione accesso alla rete.


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**ID \_ IN CONFLITTO DI PROTEZIONE ACCESSO ALLA RETE \_ \_ E**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270003L)
</dt> <dt>



L'ID entità è in conflitto con un ID entità già registrato.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ NO \_ CACHED \_ SOH**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270004L)
</dt> <dt>



Non è presente [**alcun SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) memorizzato nella cache.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**PROTEZIONE \_ ACCESSO ALLA RETE ANCORA \_ \_ ASSOCIATA**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270005L)
</dt> <dt>



L'entità è ancora associata al sistema di Protezione accesso alla rete.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**PROTEZIONE \_ ACCESSO ALLA RETE E NON \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270006L)
</dt> <dt>



L'entità non è registrata nel sistema di Protezione accesso alla rete.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**PROTEZIONE \_ ACCESSO ALLA RETE NON \_ \_ INIZIALIZZATA**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270007L)
</dt> <dt>



L'entità non viene inizializzata con il sistema di Protezione accesso alla rete.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**ID DI PROTEZIONE ACCESSO ALLA RETE NON \_ \_ \_ CORRISPONDENTE**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270008L)
</dt> <dt>



Gli ID di correlazione nella richiesta [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) e nella risposta **SoH** non corrispondono.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**PROTEZIONE \_ ACCESSO ALLA RETE E NON IN \_ \_ SOSPESO**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270009L)
</dt> <dt>



Il completamento è stato indicato in una richiesta non attualmente in sospeso.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ID E DI PROTEZIONE ACCESSO ALLA RETE NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x8027000AL)
</dt> <dt>



L'ID del componente Protezione accesso alla rete non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MAXSIZE TROPPO \_ \_ PICCOLO**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x8027000BL)
</dt> <dt>



Le dimensioni massime della connessione sono troppo piccole per un pacchetto SoH.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**SERVIZIO \_ PROTEZIONE ACCESSO ALLA RETE E NON IN \_ \_ \_ ESECUZIONE**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x8027000CL)
</dt> <dt>



Il servizio NapAgent non è in esecuzione.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**CERTIFICATO S DI PROTEZIONE ACCESSO \_ \_ ALLA RETE GIÀ \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x0027000DL) 
</dt> <dt>



Un certificato è già presente nell'archivio certificati.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**ENTITÀ \_ DI PROTEZIONE ACCESSO ALLA RETE E \_ \_ DISABILITATA**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x8027000EL)
</dt> <dt>



L'entità è disabilitata con il servizio NapAgent.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**ERRORE \_ DI NAP E \_ NETSH \_ \_ GROUPPOLICY**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x8027000FL)
</dt> <dt>



Criteri di gruppo non è configurato.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**TROPPE \_ CHIAMATE DI PROTEZIONE ACCESSO ALLA \_ \_ \_ RETE E**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270010L)
</dt> <dt>



Troppe chiamate simultanee.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**CONFIGURAZIONE \_ DI PROTEZIONE ACCESSO ALLA RETE E \_ \_ SHV \_ ESISTENTE**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270011L)
</dt> <dt>



La configurazione SHV esiste già.

> [!Note]  
> Supportato in Windows 7 o versione successiva.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**CONFIGURAZIONE \_ DI PROTEZIONE ACCESSO ALLA RETE E \_ \_ SHV NON \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270012L)
</dt> <dt>



Configurazione SHV non trovata.

> [!Note]  
> Supportato in Windows 7 o versione successiva.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**TIMEOUT \_ DI PROTEZIONE ACCESSO ALLA RETE E \_ \_ SHV**
</dt> <dd> <dl> <dt>

\_TYPEDEF \_ HRESULT \_ (0x80270013L)
</dt> <dt>



Timeout shv nella richiesta.

> [!Note]  
> Supportato in Windows 7 o versione successiva.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti di Protezione accesso alla rete**](nap-constants.md)
</dt> </dl>

 

 





