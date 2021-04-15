---
description: Consente di decrittografare un messaggio tramite digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: Funzione DecryptMessage (digest)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5363a5efc79d78c9c88e4a817c1c341e0e0f9c02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485253"
---
# <a name="decryptmessage-digest-function"></a>Funzione DecryptMessage (digest)

La funzione **DecryptMessage (digest)** decrittografa un messaggio. Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.

Il [*Security Support Provider*](../secgloss/s-gly.md) digest (SSP) fornisce la riservatezza di crittografia e decrittografia per i messaggi scambiati tra client e server solo come meccanismo SASL.

> [!Note]  
> [**EncryptMessage (digest)**](encryptmessage--digest.md) e **DecryptMessage (digest)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia. Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.

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

*phContext* \[ in\]

Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per decrittografare il messaggio.

*PMessage* \[ in uscita\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Almeno uno di questi deve essere di tipo SECBUFFER \_ Data. Il buffer contiene il messaggio crittografato. Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.

Quando si usa il provider di servizi condivisi del digest, su input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno di questi deve essere di tipo SECBUFFER \_ data o SECBUFFER \_ Stream e deve contenere il messaggio crittografato.

*MessageSeqNo* \[ in\]

Numero di sequenza previsto dall'applicazione di trasporto, se disponibile. Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.

Quando si utilizza SSP digest, questo parametro deve essere impostato su zero. SSP digest gestisce internamente i numeri di sequenza.

*pfQOP* \[ out\]

Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.

Questo parametro può essere uno dei flag seguenti.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Quando si utilizza il provider di servizi condivisi del digest, utilizzare questo flag quando il [*contesto di sicurezza*](../secgloss/s-gly.md) è impostato in modo da verificare solo la [*firma*](../secgloss/s-gly.md) . Per ulteriori informazioni, vedere [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>

## <a name="return-value"></a>Valore restituito

Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.

Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.

| Codice restituito                         | Descrizione                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ buffer \_ troppo \_ piccolo**      | Il buffer dei messaggi è troppo piccolo. Utilizzato con il provider SSP del digest.                                                                                                                   |
| **\_sistema di crittografia sec E \_ \_ \_ non valido** | La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata. Utilizzato con il provider SSP del digest.                                                                                       |
| **SEC \_ E \_ messaggio incompleto \_**     | I dati nel buffer di input sono incompleti. L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (digest)**](decryptmessage--digest.md) . |
| **\_handle sec E \_ non valido \_**         | Handle di contesto non valido specificato nel parametro *phContext* . Utilizzato con il provider SSP del digest.                                                                     |
| **SEC \_ E \_ messaggio \_ modificato**        | Il messaggio è stato modificato. Utilizzato con il provider SSP del digest.                                                                                                                      |
| **SEC \_ E \_ fuori \_ \_ sequenza**       | Il messaggio non è stato ricevuto nella sequenza corretta.                                                                                                                        |
| **SEC \_ E \_ qop \_ non \_ supportati**     | Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) . Utilizzato con il provider SSP del digest.                           |

## <a name="remarks"></a>Commenti

A volte un'applicazione legge i dati dalla parte remota, tenta di decrittografarli usando **DecryptMessage (digest)** e rileva che **DecryptMessage (digest)** è riuscito, ma i buffer di output sono vuoti. Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.

**Windows XP:** Questa funzione è nota anche come **UnsealMessage**. Le applicazioni devono ora usare solo **DecryptMessage (digest)** .

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
- [**EncryptMessage (digest)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
