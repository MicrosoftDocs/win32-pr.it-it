---
description: Decrittografa un messaggio usando Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: Funzione DecryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6bfbb354be9f3553e5369b8ce1f8b4260eab8ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750042"
---
# <a name="decryptmessage-schannel-function"></a>Funzione DecryptMessage (Schannel)

La funzione **DecryptMessage (Schannel)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.


Questa funzione viene utilizzata anche con il [*Security Support Provider*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) Schannel (SSP) per segnalare una richiesta da un mittente del messaggio per una rinegoziazione (rollforward) degli attributi di connessione o per un arresto della connessione.

> [!Note]  
> [**EncryptMessage (Schannel)**](encryptmessage--schannel.md) e **DecryptMessage (Schannel)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.


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

*phContext* \[ in\]


Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) da utilizzare per decrittografare il messaggio.

*PMessage* \[ in uscita\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno di questi può essere di tipo SECBUFFER \_ Data. Il buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

Quando si usa SSP Schannel con contesti non orientati alla connessione, in input la struttura deve contenere quattro strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Esattamente un buffer deve essere di tipo SECBUFFER \_ e contenere un messaggio crittografato, che viene decrittografato sul posto. I buffer rimanenti vengono usati per l'output e devono essere di tipo SECBUFFER \_ vuoto. Per i contesti orientati alla connessione, \_ è necessario specificare un buffer del tipo di dati SECBUFFER, come indicato per i contesti non basati sulla connessione. Inoltre, \_ è necessario fornire anche un secondo buffer di tipo di token SECBUFFER che contiene un token di sicurezza.

*MessageSeqNo* \[ in\]

Numero di sequenza previsto dall'applicazione di trasporto, se disponibile. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa i numeri di sequenza.

*pfQOP* \[ out\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Quando si usa SSP Schannel, questo parametro non viene usato e deve essere impostato su **null**.

Questo parametro può essere il seguente flag.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **\_handle sec E \_ non valido \_**     | Handle di contesto non valido specificato nel parametro *phContext* . Usato con SSP Schannel.     |
| **SEC \_ E \_ token non valido \_**      | Il tipo dei buffer non è corretto o non è stato trovato alcun buffer di tipo SECBUFFER \_ . Usato con SSP Schannel.  |
| **SEC \_ E \_ messaggio \_ modificato**    | Il messaggio è stato modificato. Usato con SSP Schannel.                                                      |
| **SEC \_ E \_ fuori \_ \_ sequenza**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                          |
| **\_contesto sec \_ I \_ scaduto**    | Il mittente del messaggio ha terminato di utilizzare la connessione ed è stato avviato un arresto. Per informazioni sull'avvio o il riconoscimento di un arresto, vedere [chiusura di una connessione Schannel](shutting-down-an-schannel-connection.md). Usato con SSP Schannel. |
| **SEC \_ I \_ rinegoziati**         | Per la parte remota è richiesta una nuova sequenza di handshake o l'applicazione ha appena avviato un arresto. Tornare al ciclo di negoziazione e chiamare [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) o [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md), passare SECBUFFER_EXTRA restituiti da DecryptMessage (). La rinegoziazione non è supportata per la modalità kernel Schannel. Il chiamante deve ignorare questo valore restituito o arrestare la connessione. Se il valore viene ignorato, il client o il server potrebbe arrestare la connessione come risultato. |


## <a name="remarks"></a>Commenti

A volte un'applicazione legge i dati dalla parte remota, tenta di decrittografarla usando **DecryptMessage (Schannel)** e rileva che **DecryptMessage (Schannel)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.

Quando si utilizza SSP Schannel, la funzione [**DecryptMessage (generale)**](decryptmessage--general.md) restituisce il contesto di sec \_ i \_ \_ scaduto quando il mittente del messaggio chiude la connessione. Per informazioni sull'avvio o il riconoscimento di un arresto, vedere [chiusura di una connessione Schannel](shutting-down-an-schannel-connection.md).

Se si usa TLS 1,0, potrebbe essere necessario chiamare questa funzione più volte, modificando il buffer di input per ogni chiamata, per decrittografare un intero messaggio.


La funzione **DecryptMessage (Schannel)** restituisce sec \_ i \_ rinegoziare quando il mittente del messaggio vuole rinegoziare la connessione ([*contesto di sicurezza*](../secgloss/s-gly.md)). Un'applicazione gestisce una rinegoziazione richiesta chiamando [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (lato server) o [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) (lato client) e passare SECBUFFER_EXTRA restituiti da DecryptMessage (). Dopo che la chiamata iniziale restituisce un valore, procedere come se l'applicazione creasse una nuova connessione. Per ulteriori informazioni, vedere [creazione di un contesto di sicurezza Schannel](creating-an-schannel-security-context.md).


## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]          |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
