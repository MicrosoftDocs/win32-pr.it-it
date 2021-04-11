---
description: Decrittografa un messaggio.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: Funzione DecryptMessage (General) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: a05906c721d9046920c465fdfdf6b1c790b06640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226316"
---
# <a name="decryptmessage-general-function"></a>Funzione DecryptMessage (General)

La funzione **DecryptMessage (generale)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.

Il [*Security Support Provider*](../secgloss/s-gly.md) digest (SSP) fornisce la riservatezza di crittografia e decrittografia per i messaggi scambiati tra client e server solo come meccanismo SASL.

Questa funzione viene usata anche con SSP Schannel per segnalare una richiesta da un mittente del messaggio per una rinegoziazione (rollforward) degli attributi di connessione o per un arresto della connessione.

> [!Note]  
> [**EncryptMessage (generale)**](encryptmessage--general.md) e **DecryptMessage (generale)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

 

Per informazioni sull'utilizzo di questa funzione con un SSP specifico, vedere gli argomenti seguenti.



| Argomento                                                            | Descrizione                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (digest)**](decryptmessage--digest.md)       | Consente di decrittografare un messaggio tramite digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Consente di decrittografare un messaggio utilizzando Kerberos.  |
| [**DecryptMessage (negoziazione)**](decryptmessage--negotiate.md) | Consente di decrittografare un messaggio tramite Negotiate. |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Consente di decrittografare un messaggio utilizzando NTLM.      |
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

*phContext* \[ in\]
</dt> <dd>

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per decrittografare il messaggio.

</dd> <dt>

*PMessage* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno di questi può essere di tipo SECBUFFER \_ Data. Il buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

Quando si usa il provider di servizi condivisi del digest, su input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno di questi deve essere di tipo SECBUFFER \_ data o SECBUFFER \_ Stream e deve contenere il messaggio crittografato.

Quando si usa SSP Schannel con contesti non orientati alla connessione, in input la struttura deve contenere quattro strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Esattamente un buffer deve essere di tipo SECBUFFER \_ e contenere un messaggio crittografato, che viene decrittografato sul posto. I buffer rimanenti vengono usati per l'output e devono essere di tipo SECBUFFER \_ vuoto. Per i contesti orientati alla connessione, \_ è necessario specificare un buffer del tipo di dati SECBUFFER, come indicato per i contesti non basati sulla connessione. Inoltre, \_ è necessario fornire anche un secondo buffer di tipo di token SECBUFFER che contiene un token di sicurezza.

</dd> <dt>

*MessageSeqNo* \[ in\]
</dt> <dd>

Numero di sequenza previsto dall'applicazione di trasporto, se disponibile. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.

Quando si utilizza SSP digest, questo parametro deve essere impostato su zero. SSP digest gestisce internamente i numeri di sequenza.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa i numeri di sequenza.

</dd> <dt>

*pfQOP* \[ out\]
</dt> <dd>

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Quando si usa SSP Schannel, questo parametro non viene usato e deve essere impostato su **null**.

Questo parametro può essere uno dei flag seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Quando si utilizza il provider di servizi condivisi del digest, utilizzare questo flag quando il [*contesto di sicurezza*](../secgloss/s-gly.md) è impostato in modo da verificare solo la [*firma*](../secgloss/s-gly.md) . Per ulteriori informazioni, vedere [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ buffer \_ troppo \_ piccolo**</dt> </dl>      | Il buffer dei messaggi è troppo piccolo. Utilizzato con il provider SSP del digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**\_sistema di crittografia sec E \_ \_ \_ non valido**</dt> </dl> | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata. Utilizzato con il provider SSP del digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ E \_ messaggio incompleto \_**</dt> </dl>     | I dati nel buffer di input sono incompleti. L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (generale)**](decryptmessage--general.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>         | Handle di contesto non valido specificato nel parametro *phContext* . Usato con i SSP digest e Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>          | Il tipo dei buffer non è corretto o non è stato trovato alcun buffer di tipo SECBUFFER \_ . Usato con SSP Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ messaggio \_ modificato**</dt> </dl>        | Il messaggio è stato modificato. Usato con i SSP digest e Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ fuori \_ \_ sequenza**</dt> </dl>       | Il messaggio non è stato ricevuto nella sequenza corretta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ qop \_ non \_ supportati**</dt> </dl>     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) . Utilizzato con il provider SSP del digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**\_contesto sec \_ I \_ scaduto**</dt> </dl>        | Il mittente del messaggio ha terminato di utilizzare la connessione ed è stato avviato un arresto. Per informazioni sull'avvio o il riconoscimento di un arresto, vedere [chiusura di una connessione Schannel](shutting-down-an-schannel-connection.md). Usato con SSP Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ I \_ rinegoziati**</dt> </dl>             | Per la parte remota è richiesta una nuova sequenza di handshake o l'applicazione ha appena avviato un arresto. Tornare al ciclo di negoziazione e chiamare [**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md) o [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md), passando buffer di input vuoti. <br/> Se la funzione restituisce un buffer aggiuntivo di **tipo \_ sec \_ buffer**, questa deve essere passata alla funzione [**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md) come buffer di input.<br/> Usato con SSP Schannel.<br/> La rinegoziazione non è supportata per la modalità kernel Schannel. Il chiamante deve ignorare questo valore restituito o arrestare la connessione. Se il valore viene ignorato, il client o il server potrebbe arrestare la connessione come risultato.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si utilizza SSP Schannel, la funzione **DecryptMessage (generale)** restituisce il contesto di sec \_ i \_ \_ scaduto quando il mittente del messaggio chiude la connessione. Per informazioni sull'avvio o il riconoscimento di un arresto, vedere [chiusura di una connessione Schannel](shutting-down-an-schannel-connection.md).

Quando si usa SSP Schannel, **DecryptMessage (General)** restituisce il secondo \_ i quali viene \_ rinegoziato quando il mittente del messaggio vuole rinegoziare la connessione ([*contesto di sicurezza*](../secgloss/s-gly.md)). Un'applicazione gestisce una rinegoziazione richiesta chiamando [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (lato server) o [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md) (lato client) e passando buffer di input vuoti. Dopo che la chiamata iniziale restituisce un valore, procedere come se l'applicazione creasse una nuova connessione. Per ulteriori informazioni, vedere [creazione di un [*contesto di sicurezza*](../secgloss/s-gly.md)Schannel](creating-an-schannel-security-context.md).

Per informazioni sull'interoperabilità con GSSAPI, vedere [interoperabilità SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
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

 

 
