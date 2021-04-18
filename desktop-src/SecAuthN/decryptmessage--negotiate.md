---
description: Consente di decrittografare un messaggio tramite Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Funzione DecryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308152"
---
# <a name="decryptmessage-negotiate-function"></a>Funzione DecryptMessage (Negotiate)

La funzione **DecryptMessage (Negotiate)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.

> [!Note]  
> [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) e **DecryptMessage (Negotiate)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

| Codice restituito                     | Descrizione                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ messaggio incompleto \_** | I dati nel buffer di input sono incompleti. L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) . |
| **SEC \_ E \_ fuori \_ \_ sequenza**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                              |

## <a name="remarks"></a>Commenti

In alcuni casi un'applicazione legge i dati dalla parte remota, tenta di decrittografarli usando **DecryptMessage (Negotiate)** e rileva che **DecryptMessage (Negotiate)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.

**Windows XP:** Questa funzione è nota anche come **UnsealMessage**. Le applicazioni devono ora usare solo **DecryptMessage (Negotiate)** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\]          |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (negoziazione)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
