---
description: Decrittografa un messaggio usando Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: Funzione DecryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: feec97f9e989270d812458cd61ff34132d118d192108c3f2372b192f2e383464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008479"
---
# <a name="decryptmessage-schannel-function"></a>Funzione DecryptMessage (Schannel)

La **funzione DecryptMessage (Schannel)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, ma eseguono e controllano un [*hash di integrità.*](../secgloss/h-gly.md)


Questa funzione viene usata anche con il provider SSP [*(Security Support Provider)*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) Schannel per segnalare una richiesta da parte di un mittente del messaggio per una rinegoziazione (redo) degli attributi di connessione o per un arresto della connessione.

> [!Note]  
> [**EncryptMessage (Schannel)**](encryptmessage--schannel.md) e **DecryptMessage (Schannel)** possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o vengono decrittografati più thread, ogni thread deve ottenere un contesto univoco.


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

*phContext* \[ Pollici\]


Handle per il contesto [*di sicurezza da*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) utilizzare per decrittografare il messaggio.

*pMessage* \[ in, out\]

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) In input, la struttura fa riferimento a una o più [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno di questi può essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

Quando si usa SSP Schannel con contesti non orientati alla connessione, nell'input la struttura deve contenere quattro [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Esattamente un buffer deve essere di tipo SECBUFFER DATA e contenere un messaggio \_ crittografato, che viene decrittografato sul posto. I buffer rimanenti vengono usati per l'output e devono essere di tipo SECBUFFER \_ EMPTY. Per i contesti orientati alla connessione, è necessario specificare un buffer del tipo di dati SECBUFFER, come indicato per i \_ contesti non orientati alla connessione. È inoltre necessario specificare un secondo buffer di tipo TOKEN SECBUFFER che contiene \_ un token di sicurezza.

*MessageSeqNo* \[ Pollici\]

Numero di sequenza previsto dall'applicazione di trasporto, se presente. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere impostato su zero.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa numeri di sequenza.

*pfQOP* \[ Cambio\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Quando si usa SSP Schannel, questo parametro non viene usato e deve essere impostato su **NULL.**

Questo parametro può essere il flag seguente.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Il messaggio non è stato crittografato, ma è stata prodotta un'intestazione o un trailer.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **HANDLE \_ SEC E NON \_ \_ VALIDO**     | Nel parametro *phContext* è stato specificato un handle di contesto non valido. Usato con il provider di servizi condivisi SCHANNEL.     |
| **TOKEN \_ SEC E NON \_ \_ VALIDO**      | I buffer sono di tipo errato o non è stato trovato alcun buffer di tipo SECBUFFER \_ DATA. Usato con il provider di servizi condivisi SCHANNEL.  |
| **MESSAGGIO \_ SEC E \_ \_ MODIFICATO**    | Il messaggio è stato modificato. Usato con il provider di servizi condivisi SCHANNEL.                                                      |
| **SEC \_ E \_ FUORI \_ \_ SEQUENZA**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                          |
| **CONTESTO \_ SEC I \_ \_ SCADUTO**    | Il mittente del messaggio ha terminato di usare la connessione e ha avviato un arresto. Per informazioni sull'avvio o sul riconoscimento di un arresto, vedere [Arresto di una connessione Schannel](shutting-down-an-schannel-connection.md). Usato con il provider di servizi condivisi SCHANNEL. |
| **SEC \_ I \_ RENEGOTIATE**         | L'entità remota richiede una nuova sequenza di handshake o l'applicazione ha appena avviato un arresto. Tornare al ciclo di negoziazione e chiamare [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) o [**InitializeSecurityContext (Schannel),**](initializesecuritycontext--schannel.md)passare SECBUFFER_EXTRA restituito da DecryptMessage(). La rinegoziazione non è supportata per la modalità kernel Schannel. Il chiamante deve ignorare questo valore restituito o arrestare la connessione. Se il valore viene ignorato, il client o il server potrebbe arrestare la connessione di conseguenza. |


## <a name="remarks"></a>Commenti

In alcuni casi un'applicazione leggerà i dati dall'entità remota, tenterà di decrittografarlo usando **DecryptMessage (Schannel)** e scoprirà che **DecryptMessage (Schannel)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale e le applicazioni devono essere in grado di gestire il problema.

Quando si usa SSP Schannel, la funzione [**DecryptMessage (Generale)**](decryptmessage--general.md) restituisce SEC I CONTEXT EXPIRED quando il mittente del messaggio \_ ha arrestato la \_ \_ connessione. Per informazioni sull'avvio o sul riconoscimento di un arresto, vedere [Arresto di una connessione Schannel](shutting-down-an-schannel-connection.md).

Se si usa TLS 1.0, potrebbe essere necessario chiamare questa funzione più volte, modificando il buffer di input in ogni chiamata, per decrittografare un intero messaggio.


La **funzione DecryptMessage (Schannel)** restituisce SEC I RENEGOTIATE quando il mittente del messaggio vuole \_ \_ rinegoziare la connessione ([*contesto di sicurezza*](../secgloss/s-gly.md)). Un'applicazione gestisce una rinegoziazione richiesta chiamando [**AcceptSecurityContext (Schannel) (lato server)**](acceptsecuritycontext--schannel.md) o [**InitializeSecurityContext (Schannel) (lato**](initializesecuritycontext--schannel.md) client) e passando SECBUFFER_EXTRA restituito da DecryptMessage(). Dopo che questa chiamata iniziale ha restituito un valore, procedere come se l'applicazione creava una nuova connessione. Per altre informazioni, vedere [Creazione di un contesto di sicurezza Schannel.](creating-an-schannel-security-context.md)


## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]          |
| Server minimo supportato | Windows Solo app desktop server 2003 \[\] |
| Intestazione                   | Sspi.h (include Security.h)               |
| Libreria                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
