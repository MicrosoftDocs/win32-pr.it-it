---
description: Decrittografa un messaggio tramite digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: Funzione DecryptMessage (Digest)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f87828263766643a10cf5400e38cabe9d3096403
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480867"
---
# <a name="decryptmessage-digest-function"></a>Funzione DecryptMessage (Digest)

La **funzione DecryptMessage (Digest)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, ma eseguono e controllano un [*hash di integrità*](../secgloss/h-gly.md).

Il provider [*SSP (Digest Security Support Provider)*](../secgloss/s-gly.md) fornisce la riservatezza di crittografia e decrittografia per i messaggi s scambiati tra client e server solo come meccanismo SASL.

> [!Note]  
> [**EncryptMessage (Digest)**](encryptmessage--digest.md) e **DecryptMessage (Digest)** possono essere chiamati contemporaneamente da due thread diversi in un singolo contesto SSPI [*(Security Support Provider Interface)*](../secgloss/s-gly.md) se un thread è in fase di crittografia e l'altro sta decrittografando. Se più thread vengono crittografati o più thread vengono decrittografati, ogni thread deve ottenere un contesto univoco.

## <a name="syntax"></a>Sintassi

```C++
SECURITY_STATUS SEC_ENTRY DecryptMessage(
  PCtxtHandle    phContext,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo,
  unsigned long  *pfQOP
);
```

## <a name="parameters"></a>Parametri

*phContext* \[ Pollici\]

Handle per il contesto [*di sicurezza da*](../secgloss/s-gly.md) utilizzare per decrittografare il messaggio.

*pMessage* \[ in, out\]

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Nell'input la struttura fa riferimento a una o [**più strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Almeno uno di questi deve essere di tipo SECBUFFER \_ DATA. Tale buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

Quando si usa il provider di servizi di configurazione digest, nell'input la struttura fa riferimento a una o più [**strutture SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno di questi deve essere di tipo SECBUFFER DATA o SECBUFFER STREAM e \_ deve \_ contenere il messaggio crittografato.

*MessageSeqNo* \[ Pollici\]

Numero di sequenza previsto dall'applicazione di trasporto, se presente. Se l'applicazione di trasporto non gestisce i numeri di sequenza, questo parametro deve essere impostato su zero.

Quando si usa il provider di servizi di configurazione digest, questo parametro deve essere impostato su zero. Il provider di servizi di configurazione digest gestisce internamente la numerazione delle sequenze.

*pfQOP* \[ Cambio\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere uno dei flag seguenti.


| valore | Significato | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Il messaggio non è stato crittografato, ma è stata prodotta un'intestazione o un trailer.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Quando si usa il provider di servizi di configurazione digest, usare questo flag quando il [*contesto di*](../secgloss/s-gly.md) sicurezza è impostato per verificare solo [*la*](../secgloss/s-gly.md) firma. Per altre informazioni, vedere [Quality of Protection.](quality-of-protection.md)<br /> | 


## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                         | Descrizione                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BUFFER \_ SEC E TROPPO \_ \_ \_ PICCOLO**      | Il buffer dei messaggi è troppo piccolo. Usato con il provider di servizi di servizi di ssp digest.                                                                                                                   |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | La [*crittografia scelta*](../secgloss/c-gly.md) per il contesto di [*sicurezza*](../secgloss/s-gly.md) non è supportata. Usato con il provider di servizi di servizi di ssp digest.                                                                                       |
| **MESSAGGIO \_ \_ INCOMPLETO \_ SEC E**     | I dati nel buffer di input sono incompleti. L'applicazione deve leggere altri dati dal server e chiamare di nuovo [**DecryptMessage (Digest).**](decryptmessage--digest.md) |
| **HANDLE SEC \_ E \_ NON \_ VALIDO**         | Nel parametro *phContext* è stato specificato un handle di contesto non valido. Usato con il provider di servizi di servizi di ssp digest.                                                                     |
| **SEC \_ E \_ MESSAGE \_ ALTERED**        | Il messaggio è stato modificato. Usato con il provider di servizi di servizi di ssp digest.                                                                                                                      |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**       | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                        |
| **SEC \_ E \_ QOP NON \_ \_ SUPPORTATO**     | La riservatezza e [*l'integrità non*](../secgloss/i-gly.md) sono supportate dal contesto [*di sicurezza*](../secgloss/s-gly.md). Usato con il provider di servizi di servizi di ssp digest.                           |

## <a name="remarks"></a>Commenti

In alcuni casi un'applicazione leggerà i dati dall'entità remota, tenterà di decrittografarlo usando **DecryptMessage (Digest)** e scoprirà che **DecryptMessage (Digest)** ha avuto esito positivo, ma i buffer di output sono vuoti. Si tratta di un comportamento normale e le applicazioni devono essere in grado di gestire il problema.

**Windows XP:** Questa funzione era nota anche come **UnsealMessage.** Le applicazioni devono ora usare **solo DecryptMessage (Digest).**

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
- [**EncryptMessage (Digest)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
