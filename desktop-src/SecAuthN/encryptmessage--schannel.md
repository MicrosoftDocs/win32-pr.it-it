---
description: Crittografa un messaggio per fornire privacy tramite Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: Funzione EncryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: de792e543a8cb67bd6b608d79832fd31a68267fc297a85e0e178d268bbc069d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008289"
---
# <a name="encryptmessage-schannel-function"></a>Funzione EncryptMessage (Schannel)

La **funzione EncryptMessage (Schannel)** crittografa un messaggio per fornire [*privacy.*](../secgloss/p-gly.md) **EncryptMessage (Schannel)** consente a un'applicazione di scegliere tra gli algoritmi [*di*](../secgloss/c-gly.md) crittografia supportati dal meccanismo scelto. La **funzione EncryptMessage (Schannel)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono invece un [*hash di*](../secgloss/h-gly.md) integrità che può essere controllato.

Quando si usa SSP Schannel, questa funzione crittografa i messaggi usando una chiave di sessione [*negoziata*](../secgloss/s-gly.md) con l'entità remota che riceverà il messaggio. L'algoritmo di crittografia è determinato dalla suite [ [*di*](../secgloss/c-gly.md) crittografia]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) in uso.

> [!Note]  
> **EncryptMessage (Schannel)** e [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o vengono decrittografati più thread, ogni thread deve ottenere un contesto univoco.

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

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

*fQOP* \[ Pollici\]

Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di*](../secgloss/s-gly.md) sicurezza può usare questo parametro per abilitare la selezione degli algoritmi di [*crittografia*](../secgloss/c-gly.md).

Questo parametro può essere il flag seguente.

| Valore                                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ ESEGUE IL WRAPPING DEI DATI \_ OOB \_**</dt> </dl> | Inviare un messaggio di avviso Schannel. In questo caso, il *parametro pMessage* deve contenere un codice evento SSL/TLS standard a due byte. Questo valore è supportato solo dal provider di servizi condivisi SCHANNEL.<br/> Ad esempio, a partire da Windows Vista, il messaggio "server hello" inviato dal server durante il protocollo di nuova autenticazione deve essere crittografato come avviso TLS.<br/> |

*pMessage* \[ in, out\]

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) In input, la struttura fa riferimento a una o più [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno di questi può essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura .

La funzione non elabora i buffer con l'attributo SECBUFFER \_ READONLY.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

*MessageSeqNo* \[ Pollici\]

Numero di sequenza assegnato dall'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere zero.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa numeri di sequenza.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                                                                                                    | Descrizione                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**</dt> </dl>      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                               |
| <dl> <dt>**CONTESTO \_ SEC E \_ \_ SCADUTO**</dt> </dl>        | L'applicazione fa riferimento a un contesto già chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere questo errore.<br/>             |
| <dl> <dt>**SISTEMA \_ DI CRITTOGRAFIA SEC E NON \_ \_ \_ VALIDO**</dt> </dl> | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata.<br/>                       |
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>    | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                           |
| <dl> <dt>**HANDLE \_ SEC E NON \_ \_ VALIDO**</dt> </dl>         | Nel parametro *phContext* è stato specificato un handle di contesto non valido.<br/>                                                                   |
| <dl> <dt>**TOKEN \_ SEC E NON \_ \_ VALIDO**</dt> </dl>          | Non è stato trovato \_ alcun buffer del tipo di dati SECBUFFER.<br/>                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**</dt> </dl>     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal [*contesto di sicurezza*](../secgloss/s-gly.md).<br/> |

## <a name="remarks"></a>Commenti

La **funzione EncryptMessage (Schannel)** crittografa un messaggio in base al messaggio e alla [*chiave di sessione*](../secgloss/s-gly.md) da un contesto di [*sicurezza*](../secgloss/s-gly.md).

Se l'applicazione [](../secgloss/s-gly.md) di trasporto ha creato il contesto di sicurezza per supportare il rilevamento delle sequenze e il chiamante fornisce un numero di sequenza, la funzione include queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

Se usato con SSP Schannel, il *parametro pMessage* deve contenere una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con i buffer seguenti.

> [!Note]  
> Questi buffer devono essere forniti nell'ordine indicato.

| Tipo di buffer                | Descrizione                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| INTESTAZIONE DEL \_ FLUSSO \_ SECBUFFER  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                        |
| DATI \_ SECBUFFER            | Contiene il [*messaggio di testo*](../secgloss/s-gly.md) non crittografato da crittografare. |
| TRAILER DEL FLUSSO SECBUFFER \_ \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                        |
| SECBUFFER \_ VUOTO           | Per uso interno. Non è necessaria alcuna inizializzazione. Le dimensioni possono essere pari a zero.                                                      |

Quando si usa SSP Schannel, determinare le dimensioni massime di ogni buffer chiamando la [**funzione QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) e specificando l'attributo SECPKG \_ ATTR \_ STREAM \_ SIZES. Questa funzione restituisce una [**struttura SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) i cui membri contengono le dimensioni massime per i buffer di intestazione (membro **cbHeader),** message **(membro cbMaximumMessage)** e trailer (membro **cbTrailer).**

Per prestazioni ottimali, le *strutture pMessage* devono essere allocate dalla memoria contigua.

**Windows XP/2000:** Questa funzione era nota anche come **SealMessage.** Le applicazioni devono ora **usare solo EncryptMessage (Schannel).**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]          |
| Server minimo supportato | Windows Solo app desktop server 2003 \[\] |
| Intestazione                   | Sspi.h (include Security.h)               |
| Libreria                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
