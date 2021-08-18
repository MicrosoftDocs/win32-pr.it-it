---
description: Decrittografa un messaggio usando Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Funzione DecryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 7da05842fc5aba4dc9c19cd530b38e0d46b640aac10b4614981c30c8863d7e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008519"
---
# <a name="decryptmessage-negotiate-function"></a>Funzione DecryptMessage (Negotiate)

La **funzione DecryptMessage (Negotiate)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, ma eseguono e controllano un [*hash di integrità.*](../secgloss/h-gly.md)

> [!Note]  
> [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) e **DecryptMessage (Negotiate)** possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o vengono decrittografati più thread, ogni thread deve ottenere un contesto univoco.

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

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) In input, la struttura fa riferimento a una o più [**strutture SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Almeno uno di questi deve essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

*MessageSeqNo* \[ Pollici\]

Numero di sequenza previsto dall'applicazione di trasporto, se presente. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere impostato su zero.

*pfQOP* \[ Cambio\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere il flag seguente.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Il messaggio non è stato crittografato, ma è stata prodotta un'intestazione o un trailer.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MESSAGGIO \_ SEC E \_ \_ INCOMPLETO** | I dati nel buffer di input sono incompleti. L'applicazione deve leggere altri dati dal server e chiamare [**nuovamente DecryptMessage (Negotiate).**](decryptmessage--negotiate.md) |
| **SEC \_ E \_ FUORI \_ \_ SEQUENZA**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                              |

## <a name="remarks"></a>Commenti

In alcuni casi un'applicazione legge i dati dall'entità remota, tenta di decrittografarlo usando **DecryptMessage (Negotiate)** e rileva che **DecryptMessage (Negotiate)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale e le applicazioni devono essere in grado di gestire il problema.

**Windows XP:** Questa funzione era nota anche come **UnsealMessage**. Le applicazioni devono ora usare **solo DecryptMessage (Negotiate).**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]          |
| Server minimo supportato | Windows Solo app desktop server 2003 \[\] |
| Intestazione                   | Sspi.h (include Security.h)               |
| Libreria                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
