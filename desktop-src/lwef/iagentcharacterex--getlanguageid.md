---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045071"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Recupera l'ID lingua impostato per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Indirizzo di una variabile che riceve l'impostazione dell'ID lingua per il carattere.

</dd> </dl>

Valore long integer che specifica l'ID lingua per il carattere. L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID di lingua primario e da un ID di lingua secondaria. Gli esempi seguenti sono valori per alcune lingue. Per determinare i valori in altre lingue, vedere la documentazione di Platform SDK.



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| Arabo (Arabia Saudita)        | 0x0401 | Italiano               | 0x0410 |
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
| Ungherese             | 0x040E |                       |        |



 

Se non si imposta questo ID lingua per il carattere, l'ID lingua del carattere sarà l'ID della lingua di sistema corrente.

Questa impostazione determina anche la lingua per l'output TTS, il testo del fumetto di parole, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale. Per determinare se è disponibile un motore di riconoscimento vocale compatibile per la lingua del carattere, usare [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se l'ID lingua è impostato su una lingua che supporta il testo bidirezionale, ad esempio l'arabo o l'ebraico, ma nel sistema in cui è in esecuzione l'applicazione non è installato il supporto bidirezionale, il testo verrà visualizzato nella parola fumetto nell'ordine logico anziché in quello visualizzato.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx: SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




