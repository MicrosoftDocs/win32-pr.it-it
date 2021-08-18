---
description: Crittografa un messaggio per fornire la privacy tramite Negotiate.
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: Funzione EncryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d4aac05a4ad030e72953cc997671b7d348cb2a598a0f56f80963f69847cdf357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008309"
---
# <a name="encryptmessage-negotiate-function"></a>Funzione EncryptMessage (Negotiate)

La **funzione EncryptMessage (Negotiate)** crittografa un messaggio per fornire [*la privacy.*](../secgloss/p-gly.md) **EncryptMessage (Negotiate)** consente all'applicazione di scegliere tra gli algoritmi [*di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto. La **funzione EncryptMessage (Negotiate)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto. Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono invece un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.

> [!Note]  
> **EncryptMessage (Negotiate)** e [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro esegue la decrittografia. Se più thread vengono crittografati o più thread vengono decrittografati, ogni thread deve ottenere un contesto univoco.

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

*phContext* \[ in \] Handle per il contesto di sicurezza [*da*](../secgloss/s-gly.md) utilizzare per crittografare il messaggio.

*fQOP* \[ in \] Flag specifici del pacchetto che indicano la qualità della protezione. Un [*pacchetto di*](../secgloss/s-gly.md) sicurezza può utilizzare questo parametro per abilitare la selezione degli algoritmi di [*crittografia*](../secgloss/c-gly.md).

Questo parametro può essere il flag seguente.

| Valore                  | Significato                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Produrre un'intestazione o un trailer, ma non crittografare il messaggio. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.

*pMessage* \[ in, out \] Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Nell'input la struttura fa riferimento a una o più [**strutture SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SECBUFFER \_ DATA. Il buffer contiene il messaggio da crittografare. Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura .

La funzione non elabora i buffer con l'attributo SECBUFFER \_ READONLY.

La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Le applicazioni che non usano SSL devono fornire [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SECBUFFER \_ PADDING.

*MessageSeqNo* \[ in \] Numero di sequenza assegnato dall'applicazione di trasporto al messaggio. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                         | Descrizione                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**      | Il buffer di output è troppo piccolo. Per altre informazioni, vedere la sezione Osservazioni.                                                                   |
| **SEC \_ E \_ CONTEXT \_ EXPIRED**        | L'applicazione fa riferimento a un contesto già chiuso. Un'applicazione scritta correttamente non dovrebbe ricevere questo errore. |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata.                                |
| **SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**    | Memoria insufficiente per completare l'azione richiesta.                                                               |
| **HANDLE SEC \_ E \_ NON \_ VALIDO**         | Nel parametro *phContext* è stato specificato un handle di contesto non valido.                                                       |
| **SEC \_ E TOKEN NON \_ \_ VALIDO**          | Non è stato trovato \_ alcun buffer del tipo di dati SECBUFFER.                                                                                            |
| **SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal contesto [*di sicurezza*](../secgloss/s-gly.md).             |

## <a name="remarks"></a>Commenti

La **funzione EncryptMessage (Negotiate)** crittografa un messaggio in base al messaggio e alla [*chiave di sessione*](../secgloss/s-gly.md) da un contesto di [*sicurezza*](../secgloss/s-gly.md).

Se l'applicazione [](../secgloss/s-gly.md) di trasporto ha creato il contesto di sicurezza per supportare il rilevamento delle sequenze e il chiamante fornisce un numero di sequenza, la funzione include queste informazioni con il messaggio crittografato. L'inclusione di queste informazioni consente di evitare la riproduzione, l'inserimento e l'eliminazione dei messaggi. Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.

> [!Note]  
> Questi buffer devono essere forniti nell'ordine indicato.

| Tipo di buffer                | Descrizione                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| INTESTAZIONE DEL FLUSSO SECBUFFER \_ \_  | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| SECBUFFER \_ DATA            | Contiene il [*messaggio di testo*](../secgloss/s-gly.md) non crittografato da crittografare. |
| TRAILER DEL FLUSSO SECBUFFER \_ \_ | Per uso interno. Non è necessaria alcuna inizializzazione.                                                |
| SECBUFFER \_ EMPTY           | Per uso interno. Non è necessaria alcuna inizializzazione. Le dimensioni possono essere pari a zero.                              |

Per ottenere prestazioni ottimali, le *strutture pMessage* devono essere allocate dalla memoria contigua.

**Windows XP:** Questa funzione era nota anche come **SealMessage.** Le applicazioni devono ora **usare solo EncryptMessage (Negotiate).**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]                |
| Server minimo supportato | Windows Solo app desktop di Server 2003 \[\]       |
| Intestazione                   | Sspi.h (includere Security.h)                     |
| Libreria                  | Secur32.lib                                     |
| DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md)
- [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
- [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
