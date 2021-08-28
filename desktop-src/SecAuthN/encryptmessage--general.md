---
description: Crittografa un messaggio per fornire privacy.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: Funzione EncryptMessage (Generale) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6645d58b753503853dae7998982a32221d1f0d14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476287"
---
# <a name="encryptmessage-general-function"></a>Funzione EncryptMessage (Generale)

La **funzione EncryptMessage (Generale)** crittografa un messaggio per fornire [*la privacy*](../secgloss/p-gly.md). **EncryptMessage (Generale)** consente a un'applicazione di scegliere tra gli algoritmi [*di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La **funzione EncryptMessage (Generale)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono invece un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

Quando si usa il provider SSP (Digest [*Security Support Provider),*](../secgloss/s-gly.md) questa funzione è disponibile solo come meccanismo SASL.

Quando si usa SSP Schannel, questa funzione crittografa i messaggi usando una chiave di sessione [*negoziata*](../secgloss/s-gly.md) con l'entità remota che riceverà il messaggio. L'algoritmo di crittografia è determinato dalla suite [ [*di*](../secgloss/c-gly.md) crittografia]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) in uso.

> [!Note]  
> **EncryptMessage (Generale)** e [**DecryptMessage (Generale)**](decryptmessage--general.md) possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro esegue la decrittografia. Se più thread vengono crittografati o più thread vengono decrittografati, ogni thread deve ottenere un contesto univoco.

Per informazioni sull'uso di questa funzione con un provider di servizi di configurazione specifico, vedere gli argomenti seguenti.

| Argomento                                                            | Descrizione                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (Digest)**](encryptmessage--digest.md)       | Crittografa un messaggio per fornire privacy tramite digest.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Crittografa un messaggio per fornire la privacy tramite Kerberos.  |
| [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) | Crittografa un messaggio per fornire la privacy tramite Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Crittografa un messaggio per fornire privacy tramite NTLM.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Crittografa un messaggio per fornire privacy tramite Schannel.  |

## <a name="syntax"></a>Sintassi

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```
## <a name="parameters"></a>Parametri

*phContext* \[ Pollici\]

Handle per il contesto [*di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

*fQOP* \[ Pollici\]

Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli algoritmi di [*crittografia*](../secgloss/c-gly.md).

Quando si usa il provider di servizi di configurazione digest, questo parametro deve essere impostato su zero.

Questo parametro può essere uno dei flag seguenti.


| valore | Significato | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Produrre un'intestazione o un trailer, ma non crittografare il messaggio.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br /> | 
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl><dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt></dl> | Inviare un messaggio di avviso Schannel. In questo caso, il <em>parametro pMessage</em> deve contenere un codice evento SSL/TLS a due byte standard. Questo valore è supportato solo da SSP Schannel.<br /> | 


*pMessage* \[ in, out\]

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Nell'input la struttura fa riferimento a una o [**più strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno di questi può essere di tipo SECBUFFER \_ DATA. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura .

La funzione non elabora i buffer con l'attributo SECBUFFER \_ READONLY.

La lunghezza della [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (General)**](querycontextattributes--general.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Quando si usa il provider di servizi di configurazione Digest, deve essere presente un secondo buffer di tipo SECBUFFER PADDING o \_ SEC BUFFER DATA per \_ \_ contenere le informazioni [*sulla*](../secgloss/d-gly.md#_security_digital_signature_gly) firma. Per ottenere le dimensioni del buffer di output, chiamare la [**funzione QueryContextAttributes (Generale)**](querycontextattributes--general.md) e specificare SECPKG \_ ATTR \_ SIZES. La funzione restituirà una [**struttura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** **e cbBlockSize.**

Le applicazioni che non usano SSL devono fornire [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SECBUFFER \_ PADDING.

*MessageSeqNo* \[ Pollici\]

Numero di sequenza assegnato al messaggio dall'applicazione di trasporto. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

Quando si usa il provider di servizi di configurazione digest, questo parametro deve essere impostato su zero. Il provider di servizi di configurazione digest gestisce internamente la numerazione delle sequenze.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa numeri di sequenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                         | Descrizione                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.                                                                                                          |
| **SEC \_ E \_ CONTEXT \_ EXPIRED**        | L'applicazione fa riferimento a un contesto già chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere questo errore.                                        |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata.                                                                       |
| **SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**    | Memoria insufficiente per completare l'azione richiesta.                                                                                                      |
| **HANDLE SEC \_ E \_ NON \_ VALIDO**         | Nel parametro *phContext* è stato specificato un handle di contesto non valido.                                                                                              |
| **SEC \_ E TOKEN NON \_ \_ VALIDO**          | Non è stato trovato \_ alcun buffer del tipo di dati SECBUFFER.                                                                                                                                   |
| **SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal contesto [*di sicurezza*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Commenti

La **funzione EncryptMessage (Generale)** crittografa un messaggio in base al messaggio e alla [*chiave di sessione*](../secgloss/s-gly.md) da un contesto di [*sicurezza*](../secgloss/s-gly.md).

Se l'applicazione [](../secgloss/s-gly.md) di trasporto ha creato il contesto di sicurezza per supportare il rilevamento delle sequenze e il chiamante fornisce un numero di sequenza, la funzione include queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni consente di evitare la riproduzione, l'inserimento e l'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

Quando si usa il provider di servizi di configurazione Digest, ottenere le dimensioni del buffer di output chiamando la [**funzione QueryContextAttributes (General)**](querycontextattributes--general.md) e specificando SECPKG \_ ATTR \_ SIZES. La funzione restituirà una [**struttura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** **e cbBlockSize.**

Se usato con SSP Schannel, il *parametro pMessage* deve contenere una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con i buffer seguenti.

> [!Note]  
> Questi buffer devono essere forniti nell'ordine indicato.

| Tipo di buffer                | Descrizione                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| INTESTAZIONE DEL FLUSSO SECBUFFER \_ \_  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| SECBUFFER \_ DATA            | Contiene il [*messaggio di testo*](../secgloss/s-gly.md) non crittografato da crittografare. |
| TRAILER DEL FLUSSO SECBUFFER \_ \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| SECBUFFER \_ EMPTY           | Per uso interno. Non è necessaria alcuna inizializzazione. Le dimensioni possono essere pari a zero.                              |

Quando si usa SSP Schannel, determinare le dimensioni massime di ogni buffer chiamando la [**funzione QueryContextAttributes (General)**](querycontextattributes--general.md) e specificando l'attributo SECPKG \_ ATTR \_ STREAM \_ SIZES. Questa funzione restituisce una struttura [**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) i cui membri contengono le dimensioni massime per i buffer di intestazione (membro **cbHeader),** message (**membro cbMaximumMessage)** e trailer (membro **cbTrailer).**

Per ottenere prestazioni ottimali, le *strutture pMessage* devono essere allocate dalla memoria contigua.

**Windows XP/2000:** Questa funzione era nota anche come **SealMessage.** Le applicazioni devono ora **usare solo EncryptMessage (Generale).**

## <a name="requirements"></a>Requisiti

| Requisito | valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]                                                            |
| Server minimo supportato | Windows Solo app desktop di Server 2003 \[\]                                                   |
| Intestazione                   | <dl> <dt>Sspi.h (includere Security.h)</dt> </dl> |
| Libreria                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Generale)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (generale)**](decryptmessage--general.md)
- [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (Generale)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
