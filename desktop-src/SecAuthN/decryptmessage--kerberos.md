---
description: Decrittografa un messaggio usando Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Funzione DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 62add8d4b33f356aeae5bbbf8fa16b19a0b5e419e0ab6c0a6847a3ed087ce726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008539"
---
# <a name="decryptmessage-kerberos-function"></a>Funzione DecryptMessage (Kerberos)

La **funzione DecryptMessage (Kerberos)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, ma eseguono e controllano un [*hash di integrità*](../secgloss/h-gly.md).

> [!Note]  
> [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) e **DecryptMessage (Kerberos)** possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro esegue la decrittografia. Se più thread vengono crittografati o più thread vengono decrittografati, ogni thread deve ottenere un contesto univoco.

## <a name="syntax"></a>Sintassi

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a>Parametri

*phContext* \[ Pollici\]

Handle per il contesto [*di sicurezza da*](../secgloss/s-gly.md) utilizzare per decrittografare il messaggio.

*pMessage* \[ in, out\]

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Nell'input la struttura fa riferimento a una o più [**strutture SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SECBUFFER \_ DATA. Il buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

*MessageSeqNo* \[ Pollici\]

Numero di sequenza previsto dall'applicazione di trasporto, se presente. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere impostato su zero.

*pfQOP* \[ Cambio\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere il flag seguente.

| Valore                  | Significato                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Il messaggio non è stato crittografato, ma è stata prodotta un'intestazione o un trailer. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ MESSAGGIO \_ INCOMPLETO** | I dati nel buffer di input sono incompleti. L'applicazione deve leggere altri dati dal server e chiamare di nuovo [**DecryptMessage (Kerberos).**](decryptmessage--kerberos.md) |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                            |

## <a name="remarks"></a>Commenti

In alcuni casi un'applicazione leggerà i dati dall'entità remota, tenterà di decrittografarlo usando **DecryptMessage (Kerberos)** e scoprirà che **DecryptMessage (Kerberos)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale e le applicazioni devono essere in grado di gestire il problema.

Per informazioni sull'interoperabilità con GSSAPI, vedere [Interoperabilità SSPI/Kerberos con GSSAPI.](sspi-kerberos-interoperability-with-gssapi.md)

**Windows XP:** Questa funzione era nota anche come **UnsealMessage.** Le applicazioni devono ora usare **solo DecryptMessage (Kerberos).**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]          |
| Server minimo supportato | Windows Solo app desktop di Server 2003 \[\] |
| Intestazione                   | Sspi.h (include Security.h)               |
| Libreria                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
