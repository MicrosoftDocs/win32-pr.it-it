---
description: Definisce una matrice a 4 byte che contiene quattro valori ASCII a 8 bit di spazio, A-Z o a-z per identificare i tag di funzionalità dello script, della lingua e del tipo di carattere OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c784fa7f6243e7e5444dcbc64c690ce7184d6ace469759c19be9de87854732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040781"
---
# <a name="opentype_tag"></a>OPENTYPE \_ TAG

Definisce una matrice a 4 byte che contiene quattro valori ASCII a 8 bit di spazio, A-Z o a-z per identificare i tag di funzionalità dello script, della lingua e del tipo di carattere OpenType.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Commenti

Gli esempi seguenti definiscono le rappresentazioni dei tag di funzionalità OpenType.

-   Il tag di funzionalità per la funzionalità della legatura è "liga".
-   I tag di lingua per romeno, urdu e persiano sono rispettivamente "ROM", "URD" e "FAR". Si noti che ognuno di questi tag termina con uno spazio.
-   I tag di script per gli script latini e arabi sono rispettivamente "latn" e "arabo".

Per altre informazioni sui tag di funzionalità OpenType e sulla specifica OpenType, vedere <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Componente ridistribuibile<br/>          | Usp10.dll versione 1.600 o successiva in Windows XPand in un secondo momento<br/>                |
| Intestazione<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Annullare la sottoscrizione di strutture](uniscribe-structures.md)
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

 

 




