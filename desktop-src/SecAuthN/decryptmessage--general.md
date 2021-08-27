---
description: Decrittografa un messaggio.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: Funzione DecryptMessage (Generale) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9dfbde6c0b4a8c46920428af3d7f700268f11690
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476917"
---
# <a name="decryptmessage-general-function"></a>Funzione DecryptMessage (Generale)

La **funzione DecryptMessage (Generale)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, ma eseguono e controllano un [*hash di integrità.*](../secgloss/h-gly.md)

Il provider [*di supporto per la*](../secgloss/s-gly.md) sicurezza digest (SSP) fornisce la riservatezza di crittografia e decrittografia per i messaggi s scambiati tra client e server solo come meccanismo SASL.

Questa funzione viene usata anche con il provider di servizi condivisi SCHANNEL per segnalare una richiesta da un mittente di messaggi per una rinegoziazione (redo) degli attributi di connessione o per un arresto della connessione.

> [!Note]  
> [**EncryptMessage (Generale)**](encryptmessage--general.md) e **DecryptMessage (Generale)** possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o vengono decrittografati più thread, ogni thread deve ottenere un contesto univoco.

 

Per informazioni sull'uso di questa funzione con un provider di servizi condivisi specifico, vedere gli argomenti seguenti.



| Argomento                                                            | Descrizione                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (digest)**](decryptmessage--digest.md)       | Decrittografa un messaggio usando digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Decrittografa un messaggio usando Kerberos.  |
| [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) | Decrittografa un messaggio usando Negotiate. |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Decrittografa un messaggio usando NTLM.      |
| [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)   | Decrittografa un messaggio usando Schannel.  |



 

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phContext* \[ Pollici\]
</dt> <dd>

Handle per il contesto [*di sicurezza da*](../secgloss/s-gly.md) utilizzare per decrittografare il messaggio.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) In input, la struttura fa riferimento a una o più [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno di questi può essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

Quando si usa digest SSP, nell'input, la struttura fa riferimento a una o più [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno di questi deve essere di tipo SECBUFFER DATA o SECBUFFER STREAM e deve \_ \_ contenere il messaggio crittografato.

Quando si usa SSP Schannel con contesti non orientati alla connessione, nell'input la struttura deve contenere quattro [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Esattamente un buffer deve essere di tipo SECBUFFER DATA e contenere un messaggio \_ crittografato, che viene decrittografato sul posto. I buffer rimanenti vengono usati per l'output e devono essere di tipo SECBUFFER \_ EMPTY. Per i contesti orientati alla connessione, è necessario specificare un buffer del tipo di dati SECBUFFER, come indicato per i \_ contesti non orientati alla connessione. È inoltre necessario specificare un secondo buffer di tipo TOKEN SECBUFFER che contiene \_ un token di sicurezza.

</dd> <dt>

*MessageSeqNo* \[ Pollici\]
</dt> <dd>

Numero di sequenza previsto dall'applicazione di trasporto, se presente. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere impostato su zero.

Quando si usa digest SSP, questo parametro deve essere impostato su zero. Il provider di servizi di gestione del digest gestisce internamente la numerazione delle sequenze.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa numeri di sequenza.

</dd> <dt>

*pfQOP* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Quando si usa SSP Schannel, questo parametro non viene usato e deve essere impostato su **NULL.**

Questo parametro può essere uno dei flag seguenti.




| valore | Significato | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Il messaggio non è stato crittografato, ma è stata prodotta un'intestazione o un trailer.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Quando si usa digest SSP, usare questo flag quando il [*contesto di*](../secgloss/s-gly.md) sicurezza è impostato per verificare solo [*la*](../secgloss/s-gly.md) firma. Per altre informazioni, vedere [Quality of Protection](quality-of-protection.md).<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**</dt> </dl>      | Il buffer dei messaggi è troppo piccolo. Usato con il provider di servizi condivisi digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SISTEMA \_ DI CRITTOGRAFIA SEC E NON \_ \_ \_ VALIDO**</dt> </dl> | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata. Usato con il provider di servizi condivisi digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**MESSAGGIO \_ SEC E \_ \_ INCOMPLETO**</dt> </dl>     | I dati nel buffer di input sono incompleti. L'applicazione deve leggere altri dati dal server e chiamare [**nuovamente DecryptMessage (Generale).**](decryptmessage--general.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**HANDLE \_ SEC E NON \_ \_ VALIDO**</dt> </dl>         | Nel parametro *phContext* è stato specificato un handle di contesto non valido. Usato con gli SSP Digest e Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**TOKEN \_ SEC E NON \_ \_ VALIDO**</dt> </dl>          | I buffer sono di tipo errato o non è stato trovato alcun buffer di tipo SECBUFFER \_ DATA. Usato con il provider di servizi condivisi SCHANNEL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**MESSAGGIO \_ SEC E \_ \_ MODIFICATO**</dt> </dl>        | Il messaggio è stato modificato. Usato con gli SSP Digest e Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ FUORI \_ \_ SEQUENZA**</dt> </dl>       | Il messaggio non è stato ricevuto nella sequenza corretta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**</dt> </dl>     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal [*contesto di sicurezza*](../secgloss/s-gly.md). Usato con il provider di servizi condivisi digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**CONTESTO \_ SEC I \_ \_ SCADUTO**</dt> </dl>        | Il mittente del messaggio ha terminato di usare la connessione e ha avviato un arresto. Per informazioni sull'avvio o sul riconoscimento di un arresto, vedere [Arresto di una connessione Schannel](shutting-down-an-schannel-connection.md). Usato con il provider di servizi condivisi SCHANNEL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ I \_ RENEGOTIATE**</dt> </dl>             | L'entità remota richiede una nuova sequenza di handshake o l'applicazione ha appena avviato un arresto. Tornare al ciclo di negoziazione e chiamare [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) o [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md), passando buffer di input vuoti. <br/> Se la funzione restituisce un buffer di tipo **SEC \_ BUFFER \_ EXTRA,** questo valore deve essere passato alla funzione [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) come buffer di input.<br/> Usato con il provider di servizi condivisi SCHANNEL.<br/> La rinegoziazione non è supportata per la modalità kernel Schannel. Il chiamante deve ignorare questo valore restituito o arrestare la connessione. Se il valore viene ignorato, il client o il server potrebbe arrestare la connessione di conseguenza.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si usa SSP Schannel, la funzione **DecryptMessage (Generale)** restituisce SEC I CONTEXT EXPIRED quando il mittente del messaggio \_ ha arrestato la \_ \_ connessione. Per informazioni sull'avvio o sul riconoscimento di un arresto, vedere [Arresto di una connessione Schannel](shutting-down-an-schannel-connection.md).

Quando si usa SSP Schannel, **DecryptMessage (Generale)** restituisce SEC I RENEGOTIATE quando il mittente del messaggio vuole \_ \_ rinegoziare la connessione ( contesto [*di sicurezza*](../secgloss/s-gly.md)). Un'applicazione gestisce una rinegoziazione richiesta chiamando [**AcceptSecurityContext (Generale) (lato server)**](acceptsecuritycontext--general.md) o [**InitializeSecurityContext (Generale) (lato client)**](initializesecuritycontext--general.md) e passando buffer di input vuoti. Dopo che questa chiamata iniziale ha restituito un valore, procedere come se l'applicazione creava una nuova connessione. Per altre informazioni, vedere [Creazione di un contesto di sicurezza Schannel. [](../secgloss/s-gly.md)](creating-an-schannel-security-context.md)

Per informazioni sull'interoperabilità con GSSAPI, vedere [Interoperabilità SSPI/Kerberos con GSSAPI.](sspi-kerberos-interoperability-with-gssapi.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**EncryptMessage (generale)**](encryptmessage--general.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
