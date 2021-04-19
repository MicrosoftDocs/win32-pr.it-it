---
description: Crittografa un messaggio per garantire la privacy tramite NTLM.
ms.assetid: 852a4624-792d-4f7d-bd3e-5a28692e2ef3
title: Funzione EncryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 4940cbc85fba6485ab78f087ce5b9bf9e4695138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317086"
---
# <a name="encryptmessage-ntlm-function"></a>Funzione EncryptMessage (NTLM)

La funzione **EncryptMessage (NTLM)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md). **EncryptMessage (NTLM)** consente a un'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La funzione **EncryptMessage (NTLM)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

> [!Note]  
> **EncryptMessage (NTLM)** e [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Produrre un'intestazione o un trailer senza crittografare il messaggio.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr></tbody></table>

*PMessage* \[ in uscita\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ Data. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.

La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) (SECPKG \_ attr \_ Stream \_ Sizes).

Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.

*MessageSeqNo* \[ in\]

Numero di sequenza assegnato all'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

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
| **SEC \_ E \_ qop \_ non \_ supportati**>    | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) .             |

## <a name="remarks"></a>Commenti

La funzione **EncryptMessage (NTLM)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).

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

**Windows XP:** Questa funzione è nota anche come **SealMessage**. Le applicazioni devono ora utilizzare solo **EncryptMessage (NTLM)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
| -------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]          |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md)
- [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)
- [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)
- [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
