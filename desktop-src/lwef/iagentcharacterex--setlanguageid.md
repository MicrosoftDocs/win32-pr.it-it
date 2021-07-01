---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119006"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Imposta l'ID lingua impostato per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Impostazione dell'ID lingua per il carattere.

</dd> </dl>

Intero lungo che specifica l'ID lingua per il carattere. L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID lingua primaria e un ID lingua secondaria. È possibile usare i valori seguenti per le lingue specificate. Per altre informazioni, vedere la documentazione di Platform SDK.



| Lingua              | ID     |  Lingua             | ID     |
|-----------------------|--------|-----------------------|--------|
| Arabo (Saudita)        | 0x0401 | Italiano               | 0x0410 |
| Basco                | 0x042d | Giapponese              | 0x0411 |
| Cinese (semplificato)  | 0x0804 | Coreano                | 0x0412 |
| Cinese (tradizionale) | 0x0404 | Norvegese             | 0x0414 |
| Croato              | 0x041A | Polacco                | 0x0415 |
| Ceco                 | 0x0405 | Portoghese (Portogallo) | 0x0816 |
| Danese                | 0x0406 | Portoghese (Brasile)   | 0x0416 |
| Olandese                 | 0x0413 | Romeno              | 0x0418 |
| Inglese (Regno Unito)     | 0x0809 | Russo               | 0x0419 |
| Inglese (Stati Uniti)          | 0x0409 | Slovacco             | 0x041B |
| Finlandese               | 0x040B | Sloveno             | 0x0424 |
| Francese                | 0x040C | Spagnolo               | 0x0C0A |
| Tedesco                | 0x0407 | Svedese               | 0x041D |
| Greco                 | 0x0408 | Thai                  | 0x041E |
| Ebraico                | 0x040D | Turco               | 0x041F |
| Ungherese             | 0x040E |                       |        |



 

Se non si imposta l'ID lingua per il carattere, il relativo ID lingua sarà l'ID lingua di sistema corrente se è installata la DLL della lingua dell'agente corrispondente. In caso contrario, la lingua del carattere sarà Inglese (Stati Uniti).

Questa proprietà determina anche la lingua per il testo del fumetto delle parole, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale. Determina anche la lingua predefinita per l'output TTS. Per determinare se è disponibile un motore di riconoscimento vocale compatibile per la lingua del carattere, usare [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Se si tenta di impostare l'ID lingua per un carattere e le risorse della lingua dell'agente, la tabella codici o un tipo di carattere visualizzato per l'ID lingua non sono disponibili, Agent restituisce un errore e l'ID lingua del carattere rimane all'ultima impostazione. L'impostazione di questa proprietà non restituisce un errore se non sono presenti motori di riconoscimento vocale corrispondenti per la lingua.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se si imposta l'ID lingua del carattere su una lingua che supporta il testo bidirezionale (ad esempio arabo o ebraico), ma nel sistema che esegue l'applicazione non è installato il supporto bidirezionale, il testo verrà visualizzato nel fumetto delle parole in ordine logico anziché di visualizzazione.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx:GetLanguageID,**](iagentcharacterex--getlanguageid.md) [**IAgentCharacterEx::GetSRModeID,**](iagentcharacterex--getsrmodeid.md) [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




