---
description: Consente di decrittografare un messaggio utilizzando Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Funzione DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129926"
---
# <a name="decryptmessage-kerberos-function"></a>Funzione DecryptMessage (Kerberos)

La funzione **DecryptMessage (Kerberos)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.

> [!Note]  
> [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) e **DecryptMessage (Kerberos)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ dati. Il buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

*MessageSeqNo* \[ in\]

Numero di sequenza previsto dall'applicazione di trasporto, se disponibile. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.

*pfQOP* \[ out\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere il seguente flag.

| Valore                  | Significato                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                     | Descrizione                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ messaggio incompleto \_** | I dati nel buffer di input sono incompleti. L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) . |
| **SEC \_ E \_ fuori \_ \_ sequenza**   | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                            |

## <a name="remarks"></a>Commenti

A volte un'applicazione legge i dati dalla parte remota, tenta di decrittografarla utilizzando **DecryptMessage (Kerberos)** e rileva che **DecryptMessage (Kerberos)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.

Per informazioni sull'interoperabilità con GSSAPI, vedere [interoperabilità SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

**Windows XP:** Questa funzione è nota anche come **UnsealMessage**. Le applicazioni devono ora utilizzare solo **DecryptMessage (Kerberos)** .

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
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
