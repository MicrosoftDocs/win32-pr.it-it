---
title: Metodo IMsTscAxEvents OnLogonError
description: Chiamato quando si verifica un errore di accesso o un altro evento di accesso.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnLogonError
- Metodo OnLogonError Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnLogonError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742119"
---
# <a name="imstscaxeventsonlogonerror-method"></a>Metodo IMsTscAxEvents:: OnLogonError

Chiamato quando si verifica un errore di accesso o un altro evento di accesso.

## <a name="syntax"></a>Sintassi


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lError* \[ in\]
</dt> <dd>

Codice di errore di accesso. Questo elenco di codici non è esaustivo.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Arbitraggio \_ \_ \_ Opzioni di Bump del codice** (-5 (0xFFFFFFFB))


</dt> <dd>

Winlogon Visualizza la finestra di dialogo **contesa di sessione** .

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Arbitraggio \_ \_ \_ Accesso continuo al codice** (-2 (0xfffffffe))


</dt> <dd>

Winlogon continua con il processo di accesso.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Arbitraggio \_ \_ \_ Terminazione continua del codice** (-3 (0xFFFFFFFD))


</dt> <dd>

Winlogon termina in modo invisibile all'utente.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Arbitraggio \_ \_ \_ Finestra di dialogo codice noperm** (-6 (0xFFFFFFFA))


</dt> <dd>

Winlogon Visualizza la finestra di dialogo **Nessuna autorizzazione** .

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Arbitraggio \_ \_Finestra di \_ dialogo del codice rifiutato** (-7 (0xFFFFFFF9))


</dt> <dd>

Winlogon Visualizza la finestra di dialogo **Disconnetti rifiutato** .

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Arbitraggio \_ \_ \_ Opzioni di ricognizione del codice** (-4 (0xFFFFFFFC))


</dt> <dd>

Winlogon Visualizza la finestra di dialogo **Riconnetti** .

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Errore \_ \_Accesso al codice \_ negato** (-1 (0xFFFFFFFF))


</dt> <dd>

All'utente è stato negato l'accesso.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Accesso \_ \_ \_ Password errata non riuscita** (0 (0x0))


</dt> <dd>

Accesso non riuscito perché le credenziali di accesso non sono valide.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Accesso \_ ERRORE \_ altro** (2 (0x2))


</dt> <dd>

Si è verificato un altro errore di accesso o post-accesso. Il client Desktop remoto Visualizza una schermata di accesso all'utente.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Accesso \_ \_ \_ Password di aggiornamento non riuscita** (1 (0x1))


</dt> <dd>

La password è scaduta. Per continuare l'accesso, l'utente deve aggiornare la password.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Accesso \_ AVVISO** (3 (0x3))


</dt> <dd>

Il client Desktop remoto Visualizza una finestra di dialogo che contiene informazioni importanti per l'utente.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Stato \_ di \_Restrizione account** (-1073741714 (0xC000006E))


</dt> <dd>

Il nome utente e le informazioni di autenticazione sono validi, ma l'autenticazione è stata bloccata a causa di restrizioni relative all'account utente, ad esempio restrizioni relative all'ora del giorno.

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Stato \_ di \_Errore di accesso** (-1073741715 (0xc000006d))


</dt> <dd>

Il tentativo di accesso non è valido. Ciò è dovuto a un nome utente errato o a informazioni di autenticazione non corrette.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Stato \_ di La PASSWORD \_ deve essere \_ modificata** (-1073741276 (0xC0000224))


</dt> <dd>

La password è scaduta. Per continuare l'accesso, l'utente deve aggiornare la password.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere una notifica che si è verificato un errore di accesso.

Questo elenco di codici non è esaustivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





