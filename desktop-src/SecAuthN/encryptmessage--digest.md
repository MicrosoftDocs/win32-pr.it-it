---
description: Crittografa un messaggio per fornire privacy tramite Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Funzione EncryptMessage (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: af16238ca58449c286edd9eabb88d7bc9a3f7fa781fac360863fdd52f7296833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008429"
---
# <a name="encryptmessage-digest-function"></a>Funzione EncryptMessage (Digest)

La **funzione EncryptMessage (Digest)** crittografa un messaggio per fornire [*privacy.*](../secgloss/p-gly.md) **EncryptMessage (Digest)** consente all'applicazione di scegliere tra gli algoritmi [*di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La **funzione EncryptMessage (Digest)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono invece un [*hash di*](../secgloss/h-gly.md) integrità che può essere controllato.

Questa funzione è disponibile solo come meccanismo SASL.

> [!Note]  
> **EncryptMessage (Digest)** e [**DecryptMessage (Digest)**](decryptmessage--digest.md) possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o vengono decrittografati più thread, ogni thread deve ottenere un contesto univoco.

 

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

*phContext* \[ Pollici\]
</dt> <dd>

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

</dd> <dt>

*fQOP* \[ Pollici\]
</dt> <dd>

Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di*](../secgloss/s-gly.md) sicurezza può usare questo parametro per abilitare la selezione degli algoritmi di [*crittografia*](../secgloss/c-gly.md).

Quando si usa digest SSP, questo parametro deve essere impostato su zero.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) In input, la struttura fa riferimento a una o più [**strutture SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura .

La funzione non elabora i buffer con l'attributo SECBUFFER \_ READONLY.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Quando si usa digest SSP, deve essere presente un secondo buffer di tipo SECBUFFER PADDING o SEC BUFFER DATA per \_ \_ \_ contenere le informazioni [*sulla*](../secgloss/d-gly.md#_security_digital_signature_gly) firma. Per ottenere le dimensioni del buffer di output, chiamare la [**funzione QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e specificare SECPKG \_ ATTR \_ SIZES. La funzione restituirà una [**struttura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** **e cbBlockSize.**

Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SECBUFFER \_ PADDING.

</dd> <dt>

*MessageSeqNo* \[ Pollici\]
</dt> <dd>

Numero di sequenza assegnato dall'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere zero.

Quando si usa digest SSP, questo parametro deve essere impostato su zero. Il provider di servizi di gestione digest gestisce internamente la numerazione delle sequenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**</dt> </dl>      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                 |
| <dl> <dt>**CONTESTO \_ SEC E \_ \_ SCADUTO**</dt> </dl>        | L'applicazione fa riferimento a un contesto già chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere questo errore.<br/>                                                                                               |
| <dl> <dt>**SISTEMA \_ DI CRITTOGRAFIA SEC E NON \_ \_ \_ VALIDO**</dt> </dl> | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata.<br/>                                                                                                         |
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>    | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                             |
| <dl> <dt>**HANDLE \_ SEC E NON \_ \_ VALIDO**</dt> </dl>         | Nel parametro *phContext* è stato specificato un handle di contesto non valido.<br/>                                                                                                                                                     |
| <dl> <dt>**TOKEN \_ SEC E NON \_ \_ VALIDO**</dt> </dl>          | Non è stato trovato \_ alcun buffer del tipo di dati SECBUFFER.<br/>                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**</dt> </dl>     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal [*contesto di sicurezza*](../secgloss/s-gly.md).<br/> |



 

## <a name="remarks"></a>Commenti

La **funzione EncryptMessage (Digest)** crittografa un messaggio in base al messaggio e alla [*chiave di sessione*](../secgloss/s-gly.md) da un contesto di [*sicurezza*](../secgloss/s-gly.md).

Se l'applicazione [](../secgloss/s-gly.md) di trasporto ha creato il contesto di sicurezza per supportare il rilevamento delle sequenze e il chiamante fornisce un numero di sequenza, la funzione include queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

Quando si usa digest SSP, ottenere le dimensioni del buffer di output chiamando la [**funzione QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e specificando SECPKG \_ ATTR \_ SIZES. La funzione restituirà una [**struttura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** **e cbBlockSize.**

> [!Note]  
> Questi buffer devono essere forniti nell'ordine indicato.

 



| Tipo di buffer                           | Descrizione                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| INTESTAZIONE DEL \_ FLUSSO \_ SECBUFFER<br/>  | Per uso interno. Non è necessaria alcuna inizializzazione.<br/>                                                                        |
| DATI \_ SECBUFFER<br/>            | Contiene il [*messaggio di testo*](../secgloss/s-gly.md) non crittografato da crittografare.<br/> |
| TRAILER DEL FLUSSO SECBUFFER \_ \_<br/> | Per uso interno. Non è necessaria alcuna inizializzazione.<br/>                                                                        |
| SECBUFFER \_ VUOTO<br/>           | Per uso interno. Non è necessaria alcuna inizializzazione. Le dimensioni possono essere pari a zero.<br/>                                                      |



 

Per prestazioni ottimali, le *strutture pMessage* devono essere allocate dalla memoria contigua.

**Windows XP:** Questa funzione era nota anche come **SealMessage.** Le applicazioni devono ora **usare solo EncryptMessage (Digest).**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
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

[**QueryContextAttributes (Digest)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
