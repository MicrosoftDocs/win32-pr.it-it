---
description: Crittografa un messaggio per garantire la privacy.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: Funzione EncryptMessage (General) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3c661f5f529700db19683966783c1aa0793e376b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305864"
---
# <a name="encryptmessage-general-function"></a>Funzione EncryptMessage (General)

La funzione **EncryptMessage (generale)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md). **EncryptMessage (generale)** consente a un'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La funzione **EncryptMessage (generale)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

Quando si utilizza il digest [*Security Support Provider*](../secgloss/s-gly.md) (SSP), questa funzione è disponibile solo come meccanismo SASL.

Quando si utilizza SSP Schannel, questa funzione crittografa i messaggi utilizzando una [*chiave di sessione*](../secgloss/s-gly.md) negoziata con la parte remota che riceverà il messaggio. L'algoritmo di crittografia è determinato dal [ [](../secgloss/c-gly.md) pacchetto]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) di crittografia in uso.

> [!Note]  
> **EncryptMessage (generale)** e [**DecryptMessage (generale)**](decryptmessage--general.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

Per informazioni sull'utilizzo di questa funzione con un SSP specifico, vedere gli argomenti seguenti.

| Argomento                                                            | Descrizione                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (digest)**](encryptmessage--digest.md)       | Crittografa un messaggio per garantire la privacy tramite digest.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Crittografa un messaggio per garantire la privacy tramite Kerberos.  |
| [**EncryptMessage (negoziazione)**](encryptmessage--negotiate.md) | Crittografa un messaggio per garantire la privacy tramite Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Crittografa un messaggio per garantire la privacy tramite NTLM.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Crittografa un messaggio per garantire la privacy tramite Schannel.  |

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

Quando si utilizza SSP digest, questo parametro deve essere impostato su zero.

Questo parametro può essere uno dei flag seguenti.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Produrre un'intestazione o un trailer senza crittografare il messaggio.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr><tr class="even"><td><span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt> </dl></td><td>Inviare un messaggio di avviso di Schannel. In questo caso, il parametro <em>PMessage</em> deve contenere un codice evento SSL/TLS standard a 2 byte. Questo valore è supportato solo dall'SSP Schannel.<br/></td></tr></tbody></table>

*PMessage* \[ in uscita\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno di questi può essere di tipo SECBUFFER \_ Data. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.

La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (generale)**](querycontextattributes--general.md) (SECPKG \_ attr \_ Stream \_ Sizes).

Quando si usa il provider di servizi condivisi del digest, è necessario che sia presente un secondo buffer di tipo SECBUFFER \_ Padding o sec \_ buffer \_ data per contenere le informazioni sulla [*firma*](../secgloss/d-gly.md#_security_digital_signature_gly) . Per ottenere le dimensioni del buffer di output, chiamare la funzione [**QueryContextAttributes (General)**](querycontextattributes--general.md) e specificare SECPKG \_ attr \_ sizes. La funzione restituirà una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** e **cbBlockSize** .

Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.

*MessageSeqNo* \[ in\]

Numero di sequenza assegnato all'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

Quando si utilizza SSP digest, questo parametro deve essere impostato su zero. SSP digest gestisce internamente i numeri di sequenza.

Quando si usa SSP Schannel, questo parametro deve essere impostato su zero. SSP Schannel non usa i numeri di sequenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                         | Descrizione                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ buffer \_ troppo \_ piccolo**      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.                                                                                                          |
| **\_contesto sec \_ E \_ scaduto**        | L'applicazione fa riferimento a un contesto che è già stato chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere l'errore.                                        |
| **\_sistema di crittografia sec E \_ \_ \_ non valido** | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.                                                                       |
| **SEC \_ E \_ memoria insufficiente \_**    | La memoria disponibile non è sufficiente per completare l'azione richiesta.                                                                                                      |
| **\_handle sec E \_ non valido \_**         | Handle di contesto non valido specificato nel parametro *phContext* .                                                                                              |
| **SEC \_ E \_ token non valido \_**          | Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.                                                                                                                                   |
| **SEC \_ E \_ qop \_ non \_ supportati**     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) . |

## <a name="remarks"></a>Commenti

La funzione **EncryptMessage (generale)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).

Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

Quando si usa il provider di servizi condivisi del digest, ottenere le dimensioni del buffer di output chiamando la funzione [**QueryContextAttributes (General)**](querycontextattributes--general.md) e specificando SECPKG \_ attr \_ sizes. La funzione restituirà una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** e **cbBlockSize** .

Se usato con SSP Schannel, il parametro *PMessage* deve contenere una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con i buffer seguenti.

> [!Note]  
> Questi buffer devono essere specificati nell'ordine indicato.

| Tipo di buffer                | Descrizione                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_intestazione del flusso SECBUFFER \_  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| \_dati SECBUFFER            | Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare. |
| \_trailer del flusso SECBUFFER \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| SECBUFFER \_ vuoto           | Per uso interno. Non è necessaria alcuna inizializzazione. Size può essere zero.                              |

Quando si usa SSP Schannel, determinare le dimensioni massime di ogni buffer chiamando la funzione [**QueryContextAttributes (generale)**](querycontextattributes--general.md) e specificando l' \_ attributo SECPKG attr \_ Stream \_ sizes. Questa funzione restituisce una [**struttura \_ SecPkgContext StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) i cui membri contengono le dimensioni massime per i buffer di intestazione (membro **cbHeader** ), messaggio (membro **CbMaximumMessage** ) e Trailer (membro **cbTrailer** ).

Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.

**Windows XP/2000:** Questa funzione è nota anche come **SealMessage**. Le applicazioni dovrebbero ora usare solo **EncryptMessage (generale)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]                                                            |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\]                                                   |
| Intestazione                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (generale)**](decryptmessage--general.md)
- [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (generale)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
