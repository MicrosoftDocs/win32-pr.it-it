---
description: La chiave del registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai caratteri definiti dall'utente finale (EUDCs) per una determinata tabella codici.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317153"
---
# <a name="eudc"></a>EUDC

La chiave del registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai [caratteri definiti dall'utente finale (EUDCs)](end-user-defined-characters.md) per una determinata tabella codici. Dispone del seguente percorso del registro di sistema:

HKEY \_ \_ utente corrente \\ EUDC

Il formato è:

EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName

dove:



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nome predefinito utilizzato per impostare il tipo di carattere predefinito del sistema. Non esiste alcun tipo di carattere EUDC predefinito di sistema, a meno che questa voce non venga specificata in modo esplicito.     |
| TrueTypeFontTypeface     | Nome definito dall'utente associato a un tipo di carattere TrueType non EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Stringa costituita dal nome file di un file del tipo di carattere EUDC separato. Questo file identifica un tipo di carattere da associare a TrueTypeFontTypeface. |



 

Nell'esempio seguente viene illustrata la chiave EUDC per la tabella codici 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



Nell'esempio seguente viene impostato il tipo di carattere EUDC predefinito di sistema come EUDC. ttf e vengono associati i tipi di carattere EUDC separati Mineudc. ttf e Goteudc. ttf con i nomi dei tipi di carattere MS Mincho e MS Gothic, rispettivamente.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Quando la tabella codici di Windows (System ACP) associata alla lingua per i programmi non Unicode corrisponde alla sottochiave, il sottosistema GDI Cerca le coppie di valori della sottochiave per ottenere le informazioni di visualizzazione relative al carattere. Per prima cosa cerca un nome che corrisponda al tipo di carattere corrente. Se non è presente alcun valore, viene esaminato il valore SystemDefaultEUDCFont. Se non è definito alcun valore, GDI considera il carattere come non definito.

Si noti che il testo non deve essere presente nella tabella codici di Windows. Si supponga, ad esempio, che la tabella codici abbia l'identificatore 1252, la tabella codici di Windows predefinita per la lingua inglese. Un'applicazione passa il singolo punto di codice Unicode U + E000, nell'area di utilizzo privato Unicode (PUA), a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). In questo caso, GDI esamina i valori del registro di sistema sotto 1252 per ottenere le informazioni sul carattere per le proprietà di visualizzazione dei caratteri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci del registro di sistema EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
