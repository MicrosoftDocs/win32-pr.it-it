---
description: Crittografa un messaggio per garantire la privacy tramite digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Funzione EncryptMessage (digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305865"
---
# <a name="encryptmessage-digest-function"></a>Funzione EncryptMessage (digest)

La funzione **EncryptMessage (digest)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md). **EncryptMessage (digest)** consente all'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La funzione **EncryptMessage (digest)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

Questa funzione è disponibile solo come meccanismo SASL.

> [!Note]  
> **EncryptMessage (digest)** e [**DecryptMessage (digest)**](decryptmessage--digest.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

 

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
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

Quando si utilizza SSP digest, questo parametro deve essere impostato su zero.

</dd> <dt>

*PMessage* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ Data. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.

La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) (SECPKG \_ attr \_ Stream \_ Sizes).

Quando si usa il provider di servizi condivisi del digest, è necessario che sia presente un secondo buffer di tipo SECBUFFER \_ Padding o sec \_ buffer \_ data per contenere le informazioni sulla [*firma*](../secgloss/d-gly.md#_security_digital_signature_gly) . Per ottenere le dimensioni del buffer di output, chiamare la funzione [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) e specificare SECPKG \_ attr \_ sizes. La funzione restituirà una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** e **cbBlockSize** .

Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.

</dd> <dt>

*MessageSeqNo* \[ in\]
</dt> <dd>

Numero di sequenza assegnato all'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

Quando si utilizza SSP digest, questo parametro deve essere impostato su zero. SSP digest gestisce internamente i numeri di sequenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ buffer \_ troppo \_ piccolo**</dt> </dl>      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                 |
| <dl> <dt>**\_contesto sec \_ E \_ scaduto**</dt> </dl>        | L'applicazione fa riferimento a un contesto che è già stato chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere l'errore.<br/>                                                                                               |
| <dl> <dt>**\_sistema di crittografia sec E \_ \_ \_ non valido**</dt> </dl> | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.<br/>                                                                                                         |
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl>    | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                             |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>         | Handle di contesto non valido specificato nel parametro *phContext* .<br/>                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>          | Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.<br/>                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ qop \_ non \_ supportati**</dt> </dl>     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) .<br/> |



 

## <a name="remarks"></a>Commenti

La funzione **EncryptMessage (digest)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).

Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

Quando si usa il provider di servizi condivisi del digest, ottenere le dimensioni del buffer di output chiamando la funzione [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) e specificando SECPKG \_ attr \_ sizes. La funzione restituirà una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** e **cbBlockSize** .

> [!Note]  
> Questi buffer devono essere specificati nell'ordine indicato.

 



| Tipo di buffer                           | Descrizione                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_intestazione del flusso SECBUFFER \_<br/>  | Per uso interno. Non è necessaria alcuna inizializzazione.<br/>                                                                        |
| \_dati SECBUFFER<br/>            | Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare.<br/> |
| \_trailer del flusso SECBUFFER \_<br/> | Per uso interno. Non è necessaria alcuna inizializzazione.<br/>                                                                        |
| SECBUFFER \_ vuoto<br/>           | Per uso interno. Non è necessaria alcuna inizializzazione. Size può essere zero.<br/>                                                      |



 

Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.

**Windows XP:** Questa funzione è nota anche come **SealMessage**. Le applicazioni devono ora usare solo **EncryptMessage (digest)** .

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

[**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (digest)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (digest)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
