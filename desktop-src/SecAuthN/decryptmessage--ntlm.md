---
description: Decrittografa un messaggio tramite NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Funzione DecryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f73159c1b6e9fbe3d6d9c282ffdb05271e29583b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481047"
---
# <a name="decryptmessage-ntlm-function"></a>Funzione DecryptMessage (NTLM)

La **funzione DecryptMessage (NTLM)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, ma eseguono e controllano un [*hash di integrità*](../secgloss/h-gly.md).

> [!Note]  
> [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) e **DecryptMessage (NTLM)** possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o più thread vengono decrittografati, ogni thread deve ottenere un contesto univoco.

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

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Nell'input la struttura fa riferimento a una o [**più strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Almeno uno di questi deve essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

*MessageSeqNo* \[ Pollici\]

Numero di sequenza previsto dall'applicazione di trasporto, se presente. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere impostato su zero.

*pfQOP* \[ Cambio\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere il flag seguente.


| valore | Significato | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Il messaggio non è stato crittografato, ma è stata prodotta un'intestazione o un trailer.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br /> | 


## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MESSAGGIO \_ \_ INCOMPLETO \_ SEC E** | I dati nel buffer di input sono incompleti. L'applicazione deve leggere altri dati dal server e chiamare di nuovo [**DecryptMessage (NTLM).**](decryptmessage--ntlm.md) |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                    |

## <a name="remarks"></a>Commenti

In alcuni casi un'applicazione leggerà i dati dall'entità remota, tenterà di decrittografarlo usando **DecryptMessage (NTLM)** e scoprirà che **DecryptMessage (NTLM)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale e le applicazioni devono essere in grado di gestire il problema.

**Windows XP:** Questa funzione era nota anche come **UnsealMessage.** Le applicazioni devono ora usare **solo DecryptMessage (NTLM).**

## <a name="requirements"></a>Requisiti

| Requisito | valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\]          |
| Server minimo supportato | Windows Solo app desktop di Server 2003 \[\] |
| Intestazione                   | Sspi.h (includere Security.h)               |
| Libreria                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
