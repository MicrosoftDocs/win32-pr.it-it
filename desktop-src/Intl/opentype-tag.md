---
description: Definisce una matrice di 4 byte che contiene i valori ASCII a 4 8 bit, A-Z o a-z per identificare gli script OpenType, il linguaggio e i tag della funzionalità del tipo di carattere.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309499"
---
# <a name="opentype_tag"></a>\_tag OPENTYPE

Definisce una matrice di 4 byte che contiene i valori ASCII a 4 8 bit, A-Z o a-z per identificare gli script OpenType, il linguaggio e i tag della funzionalità del tipo di carattere.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Commenti

Negli esempi seguenti vengono definite le rappresentazioni dei tag della funzionalità OpenType.

-   Il tag di funzionalità per la funzionalità di legatura è "Liga".
-   I tag di lingua per Romeno, Urdu e persiano sono rispettivamente "ROM", "URD" e "lontano". Si noti che ognuno di questi tag termina con uno spazio.
-   I tag di script per gli script latini e arabi sono rispettivamente "Latn" e "Arab".

Per ulteriori informazioni sui tag delle funzionalità OpenType e sulla specifica OpenType, vedere <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Componente ridistribuibile<br/>          | Usp10.dll versione 1,600 o successiva in Windows Espandi in un secondo momento<br/>                |
| Intestazione<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Strutture Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




