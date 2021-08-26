---
description: La chiave del Registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai caratteri definiti dall'utente finale (EUDC) per una determinata tabella codici.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: Eudc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a7509364545d9de01d4480a58d4e6af8043c30fa8f74db0fdbaf24e252e298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082991"
---
# <a name="eudc"></a>Eudc

La chiave del Registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai caratteri definiti dall'utente [finale (EUDC)](end-user-defined-characters.md) per una determinata tabella codici. Il percorso del Registro di sistema è il seguente:

HKEY \_ CURRENT \_ USER \\ EUDC

Il formato è:

EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName

dove:



| Valore                         | Descrizione                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nome predefinito usato per impostare il tipo di carattere predefinito del sistema. Non esiste alcun tipo di carattere EUDC predefinito di sistema, a meno che questa voce non venga specificata in modo esplicito.     |
| TrueTypeFontTypeface     | Nome definito dall'utente associato a un tipo di carattere TrueType non EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Stringa costituita dal nome file di un file del tipo di carattere EUDC separato. Questo file identifica un tipo di carattere da associare a TrueTypeFontTypeface. |



 

Nell'esempio seguente viene illustrata la chiave EUDC per la tabella codici 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



Nell'esempio seguente il tipo di carattere EUDC predefinito del sistema viene impostato su Eudc.ttf e vengono associati i tipi di carattere EUDC separati Mineudc.ttf e Goteudc.ttf rispettivamente ai nomi dei tipi di carattere MS Mincho e MS Fonts.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Quando la tabella codici di Windows associata alla lingua per i programmi non Unicode corrisponde alla sottochiave , il sottosistema GDI cerca le coppie di valori della sottochiave per ottenere informazioni di visualizzazione sul carattere. Cerca innanzitutto un nome corrispondente al tipo di carattere corrente. Se non è presente, esamina il valore SystemDefaultEUDCFont. Se non è definito alcun valore, GDI considera il carattere come non definito.

Si noti che il testo stesso non deve essere presente nella tabella Windows tabella codici. Si supponga, ad esempio, che la tabella codici abbia l'identificatore 1252, Windows predefinita per l'inglese. Un'applicazione passa il singolo punto di codice Unicode U+E000, nell'area di utilizzo privato Unicode (PUA), a [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext) In questo caso, GDI esamina i valori del Registro di sistema sotto 1252 per ottenere le informazioni sul tipo di carattere per le proprietà di visualizzazione dei caratteri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci del Registro di sistema EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
