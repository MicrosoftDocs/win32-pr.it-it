---
description: Crittografa un messaggio per garantire la privacy tramite Negotiate.
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: Funzione EncryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 037866088f58fa1d70939b84062161a6e4f610b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348101"
---
# <a name="encryptmessage-negotiate-function"></a>Funzione EncryptMessage (Negotiate)

La funzione **EncryptMessage (Negotiate)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md). **EncryptMessage (Negotiate)** consente all'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La funzione **EncryptMessage (Negotiate)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

> [!Note]  
> **EncryptMessage (Negotiate)** e [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

*phContext* \[ in \] un handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

*fQOP* \[ in \] flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli [*algoritmi di crittografia*](../secgloss/c-gly.md).

Questo parametro può essere il seguente flag.

| Valore                  | Significato                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Produrre un'intestazione o un trailer senza crittografare il messaggio. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.

*PMessage* \[ in, \] un puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ Data. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.

La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) (SECPKG \_ attr \_ Stream \_ Sizes).

Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.

*MessageSeqNo* \[ nel \] numero di sequenza assegnato all'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                         | Descrizione                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ buffer \_ troppo \_ piccolo**      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.                                                                   |
| **\_contesto sec \_ E \_ scaduto**        | L'applicazione fa riferimento a un contesto che è già stato chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere l'errore. |
| **\_sistema di crittografia sec E \_ \_ \_ non valido** | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.                                |
| **SEC \_ E \_ memoria insufficiente \_**    | La memoria disponibile non è sufficiente per completare l'azione richiesta.                                                               |
| **\_handle sec E \_ non valido \_**         | Handle di contesto non valido specificato nel parametro *phContext* .                                                       |
| **SEC \_ E \_ token non valido \_**          | Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.                                                                                            |
| **SEC \_ E \_ qop \_ non \_ supportati**     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) .             |

## <a name="remarks"></a>Commenti

La funzione **EncryptMessage (Negotiate)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).

Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

> [!Note]  
> Questi buffer devono essere specificati nell'ordine indicato.

| Tipo di buffer                | Descrizione                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_intestazione del flusso SECBUFFER \_  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| \_dati SECBUFFER            | Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare. |
| \_trailer del flusso SECBUFFER \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| SECBUFFER \_ vuoto           | Per uso interno. Non è necessaria alcuna inizializzazione. Size può essere zero.                              |

Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.

**Windows XP:** Questa funzione è nota anche come **SealMessage**. Le applicazioni devono ora usare solo **EncryptMessage (Negotiate)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]                |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\]       |
| Intestazione                   | SSPI. h (include Security. h)                     |
| Libreria                  | Secur32. lib                                     |
| DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (negoziazione)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (negoziazione)**](decryptmessage--negotiate.md)
- [**InitializeSecurityContext (negoziazione)**](initializesecuritycontext--negotiate.md)
- [**QueryContextAttributes (negoziazione)**](querycontextattributes--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
