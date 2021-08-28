---
description: Crittografa un messaggio per fornire la privacy tramite Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Funzione EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 89c6504fe8518e1c43d155ebce638dec1acfeb80
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476217"
---
# <a name="encryptmessage-kerberos-function"></a>Funzione EncryptMessage (Kerberos)

La **funzione EncryptMessage (Kerberos)** crittografa un messaggio per fornire [*la privacy.*](../secgloss/p-gly.md) **EncryptMessage (Kerberos)** consente a un'applicazione di scegliere tra gli algoritmi [*di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La **funzione EncryptMessage (Kerberos)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono invece un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

> [!Note]  
> **EncryptMessage (Kerberos)** e [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro esegue la decrittografia. Se più thread vengono crittografati o più thread vengono decrittografati, ogni thread deve ottenere un contesto univoco.

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

*phContext* \[ Pollici\]
</dt> <dd>

Handle per il contesto [*di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.

</dd> <dt>

*fQOP* \[ Pollici\]
</dt> <dd>

Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli algoritmi di [*crittografia*](../secgloss/c-gly.md).

Questo parametro può essere il flag seguente.


| valore | Significato | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Produrre un'intestazione o un trailer, ma non crittografare il messaggio.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br /> | 


</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Nell'input la struttura fa riferimento a una o più [**strutture SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SECBUFFER \_ DATA. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura .

La funzione non elabora i buffer con l'attributo SECBUFFER \_ READONLY.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Le applicazioni che non usano SSL devono fornire [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SECBUFFER \_ PADDING.

</dd> <dt>

*MessageSeqNo* \[ Pollici\]
</dt> <dd>

Numero di sequenza assegnato al messaggio dall'applicazione di trasporto. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**</dt> </dl>      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.                                                                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ CONTEXT \_ EXPIRED**</dt> </dl>        | L'applicazione fa riferimento a un contesto già chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere questo errore.                                                                                               |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata.                                                                                                         |
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>    | Memoria insufficiente per completare l'azione richiesta.                                                                                                                                                             |
| <dl> <dt>**HANDLE SEC \_ E \_ NON \_ VALIDO**</dt> </dl>         | Nel parametro *phContext* è stato specificato un handle di contesto non valido.                                                                                                                                                     |
| <dl> <dt>**SEC \_ E TOKEN NON \_ \_ VALIDO**</dt> </dl>          | Non è stato trovato \_ alcun buffer del tipo di dati SECBUFFER.                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**</dt> </dl>     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal contesto [*di sicurezza*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Commenti

La **funzione EncryptMessage (Kerberos)** crittografa un messaggio in base al messaggio e alla [*chiave di sessione*](../secgloss/s-gly.md) da un contesto di [*sicurezza*](../secgloss/s-gly.md).

Se l'applicazione [](../secgloss/s-gly.md) di trasporto ha creato il contesto di sicurezza per supportare il rilevamento delle sequenze e il chiamante fornisce un numero di sequenza, la funzione include queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni consente di evitare la riproduzione, l'inserimento e l'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

> [!Note]  
> Questi buffer devono essere forniti nell'ordine indicato.

| Tipo di buffer                           | Descrizione                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| INTESTAZIONE DEL FLUSSO SECBUFFER \_ \_<  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                       |
| SECBUFFER \_ DATA            | Contiene il [*messaggio di testo*](../secgloss/s-gly.md) non crittografato da crittografare. |
| TRAILER DEL FLUSSO SECBUFFER \_ \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                                        |
| SECBUFFER \_ EMPTY           | Per uso interno. Non è necessaria alcuna inizializzazione. Le dimensioni possono essere pari a zero.                                                      |

Per ottenere prestazioni ottimali, le *strutture pMessage* devono essere allocate dalla memoria contigua.

**Windows XP:** Questa funzione era nota anche come **SealMessage.** Le applicazioni devono ora **usare solo EncryptMessage (Kerberos).**

## <a name="requirements"></a>Requisiti

| Requisito | valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]          |
| Server minimo supportato | Windows Solo app desktop di Server 2003 \[\] |
| Intestazione                   | Sspi.h (includere Security.h)               |
| Libreria                  | Secur32.lib                               |
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
