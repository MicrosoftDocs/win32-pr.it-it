---
description: Crittografa un messaggio per garantire la privacy tramite Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Funzione EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233288"
---
# <a name="encryptmessage-kerberos-function"></a>Funzione EncryptMessage (Kerberos)

La funzione **EncryptMessage (Kerberos)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md). **EncryptMessage (Kerberos)** consente a un'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La funzione **EncryptMessage (Kerberos)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

> [!Note]  
> **EncryptMessage (Kerberos)** e [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

<dl> <dt>

*phContext* \[ in\]
</dt> <dd>

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

</dd> <dt>

*fQOP* \[ in\]
</dt> <dd>

Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli [*algoritmi di crittografia*](../secgloss/c-gly.md).

Questo parametro può essere il seguente flag.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Produrre un'intestazione o un trailer senza crittografare il messaggio.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr></tbody></table>

</dd> <dt>

*PMessage* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ Data. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.

La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ attr \_ Stream \_ Sizes).

Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.

</dd> <dt>

*MessageSeqNo* \[ in\]
</dt> <dd>

Numero di sequenza assegnato all'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ buffer \_ troppo \_ piccolo**</dt> </dl>      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.                                                                                                                                                                 |
| <dl> <dt>**\_contesto sec \_ E \_ scaduto**</dt> </dl>        | L'applicazione fa riferimento a un contesto che è già stato chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere l'errore.                                                                                               |
| <dl> <dt>**\_sistema di crittografia sec E \_ \_ \_ non valido**</dt> </dl> | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.                                                                                                         |
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl>    | La memoria disponibile non è sufficiente per completare l'azione richiesta.                                                                                                                                                             |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>         | Handle di contesto non valido specificato nel parametro *phContext* .                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>          | Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ qop \_ non \_ supportati**</dt> </dl>     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) . |

## <a name="remarks"></a>Commenti

La funzione **EncryptMessage (Kerberos)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).

Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

> [!Note]  
> Questi buffer devono essere specificati nell'ordine indicato.

| Tipo di buffer                           | Descrizione                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_< intestazione del flusso SECBUFFER \_  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                       |
| \_dati SECBUFFER            | Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare. |
| \_trailer del flusso SECBUFFER \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                        |
| SECBUFFER \_ vuoto           | Per uso interno. Non è necessaria alcuna inizializzazione. Size può essere zero.                                                      |

Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.

**Windows XP:** Questa funzione è nota anche come **SealMessage**. Le applicazioni devono ora utilizzare solo **EncryptMessage (Kerberos)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]          |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
