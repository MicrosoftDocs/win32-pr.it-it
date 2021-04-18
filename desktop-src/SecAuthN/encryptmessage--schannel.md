---
description: Crittografa un messaggio per garantire la privacy tramite Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: Funzione EncryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3075b2fe7e5b4167a5a8527a16009282b2fca1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317085"
---
# <a name="encryptmessage-schannel-function"></a>Funzione EncryptMessage (Schannel)

La funzione **EncryptMessage (Schannel)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md). **EncryptMessage (Schannel)** consente a un'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La funzione **EncryptMessage (Schannel)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

Quando si utilizza SSP Schannel, questa funzione crittografa i messaggi utilizzando una [*chiave di sessione*](../secgloss/s-gly.md) negoziata con la parte remota che riceverà il messaggio. L'algoritmo di crittografia è determinato dal [ [](../secgloss/c-gly.md) pacchetto]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) di crittografia in uso.

> [!Note]  
> **EncryptMessage (Schannel)** e [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

*phContext* \[ in\]

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

*fQOP* \[ in\]

Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli [*algoritmi di crittografia*](../secgloss/c-gly.md).

Questo parametro può essere il seguente flag.

| Valore                                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ Wrap \_ OOB \_ dati**</dt> </dl> | Inviare un messaggio di avviso di Schannel. In questo caso, il parametro *PMessage* deve contenere un codice evento SSL/TLS standard a 2 byte. Questo valore è supportato solo dall'SSP Schannel.<br/> Ad esempio, a partire da Windows Vista, il messaggio "Server Hello" inviato dal server durante il protocollo di riautenticazione deve essere crittografato come un avviso TLS.<br/> |

*PMessage* \[ in uscita\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno di questi può essere di tipo SECBUFFER \_ Data. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.

La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) (SECPKG \_ attr \_ Stream \_ Sizes).

*MessageSeqNo* \[ in\]

Numero di sequenza assegnato all'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa i numeri di sequenza.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                                                                                                    | Descrizione                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ buffer \_ troppo \_ piccolo**</dt> </dl>      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                               |
| <dl> <dt>**\_contesto sec \_ E \_ scaduto**</dt> </dl>        | L'applicazione fa riferimento a un contesto che è già stato chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere l'errore.<br/>             |
| <dl> <dt>**\_sistema di crittografia sec E \_ \_ \_ non valido**</dt> </dl> | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.<br/>                       |
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl>    | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                           |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>         | Handle di contesto non valido specificato nel parametro *phContext* .<br/>                                                                   |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>          | Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.<br/>                                                                                                        |
| <dl> <dt>**SEC \_ E \_ qop \_ non \_ supportati**</dt> </dl>     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) .<br/> |

## <a name="remarks"></a>Commenti

La funzione **EncryptMessage (Schannel)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).

Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

Se usato con SSP Schannel, il parametro *PMessage* deve contenere una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con i buffer seguenti.

> [!Note]  
> Questi buffer devono essere specificati nell'ordine indicato.

| Tipo di buffer                | Descrizione                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| \_intestazione del flusso SECBUFFER \_  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                        |
| \_dati SECBUFFER            | Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare. |
| \_trailer del flusso SECBUFFER \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                        |
| SECBUFFER \_ vuoto           | Per uso interno. Non è necessaria alcuna inizializzazione. Size può essere zero.                                                      |

Quando si usa SSP Schannel, determinare le dimensioni massime di ogni buffer chiamando la funzione [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) e specificando l' \_ attributo SECPKG attr \_ Stream \_ sizes. Questa funzione restituisce una [**struttura \_ SecPkgContext StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) i cui membri contengono le dimensioni massime per i buffer di intestazione (membro **cbHeader** ), messaggio (membro **CbMaximumMessage** ) e Trailer (membro **cbTrailer** ).

Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.

**Windows XP/2000:** Questa funzione è nota anche come **SealMessage**. Le applicazioni dovrebbero ora usare solo **EncryptMessage (Schannel)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]          |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
