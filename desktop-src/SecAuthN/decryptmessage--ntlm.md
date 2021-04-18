---
description: Consente di decrittografare un messaggio utilizzando NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Funzione DecryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313745"
---
# <a name="decryptmessage-ntlm-function"></a>Funzione DecryptMessage (NTLM)

La funzione **DecryptMessage (NTLM)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.

> [!Note]  
> [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) e **DecryptMessage (NTLM)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

*phContext* \[ in\]

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per decrittografare il messaggio.

*PMessage* \[ in uscita\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Almeno uno di questi deve essere di tipo SECBUFFER \_ Data. Il buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

*MessageSeqNo* \[ in\]

Numero di sequenza previsto dall'applicazione di trasporto, se disponibile. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.

*pfQOP* \[ out\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere il seguente flag.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ messaggio incompleto \_** | I dati nel buffer di input sono incompleti. L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) . |
| **SEC \_ E \_ fuori \_ \_ sequenza**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                    |

## <a name="remarks"></a>Commenti

A volte un'applicazione legge i dati dalla parte remota, tenta di decrittografarla utilizzando **DecryptMessage (NTLM)** e rileva che **DecryptMessage (NTLM)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.

**Windows XP:** Questa funzione è nota anche come **UnsealMessage**. Le applicazioni devono ora utilizzare solo **DecryptMessage (NTLM)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]          |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
