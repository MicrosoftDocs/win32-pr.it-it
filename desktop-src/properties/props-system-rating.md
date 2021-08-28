---
description: Sistema di classificazione che usa valori interi compresi tra 1 e 99. Questo è il sistema di classificazione usato dalla shell Windows Vista.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System.Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc62e69ced0f82426f19badb1aebef0453084a9b951b749aed256aa64820a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598131"
---
# <a name="systemrating"></a>System.Rating

Sistema di classificazione che usa valori interi compresi tra 1 e 99. Questo è il sistema di classificazione usato dalla shell Windows Vista.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Per la compatibilità con i sistemi ratings che usano valori compresi tra 1 e 5, vedere la [proprietà System.SimpleRating](./props-system-simplerating.md). Si noti, tuttavia, che System.SimpleRating non viene usato nella shell Windows Vista.

La tabella seguente descrive il significato del sistema di classificazione a stella usato nell'interfaccia utente della shell in termini [di valore System.Rating.]()



| System.Rating | Classificazione a stelle |
|---------------|-------------|
| 1-12          | 1 stella      |
| 13-37         | 2 stelle     |
| 38-62         | 3 stelle     |
| 63-87         | 4 stelle     |
| 88-99         | 5 stelle     |



 

Quando un utente valuta un elemento scegliendo un valore di classificazione a stella nell'interfaccia utente, i valori [System.Rating]() effettivi vengono assegnati come illustrato nella tabella seguente:



| Classificazione a stelle | Valore assegnato tramite l'interfaccia utente |
|-------------|---------------------------|
| 1 stella      | 1                         |
| 2 stelle     | 25                        |
| 3 stelle     | 50                        |
| 4 stelle     | 75                        |
| 5 stelle     | 99                        |



 

Se il file ha un [valore System.SimpleRating](./props-system-simplerating.md) anziché un valore [System.Rating,]() usare la tabella seguente per convertire e specificare i valori per System.Rating.



| System.SimpleRating | System.Rating |
|---------------------|---------------|
| 1                   | 1             |
| 2                   | 25            |
| 3                   | 50            |
| 4                   | 75            |
| 5                   | 99            |



 

Se il file contiene valori persistenti [sia System.Rating]() che [System.SimpleRating,](./props-system-simplerating.md) usare sempre il valore System.Rating quando viene richiesto direttamente, senza riferimenti a System.SimpleRating.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[proprietàDescrizione](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[Datetimeformat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
