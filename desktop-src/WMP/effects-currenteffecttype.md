---
title: EFFECTS.currentEffectType
description: L'attributo currentEffectType specifica o recupera il nome del Registro di sistema della visualizzazione corrente. Questo nome è un ID univoco definito dall'autore della visualizzazione.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- Effects.currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df55ae806781fa0924349cfe472f355cdabd2be6723148fc6100dc39efd9062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996751"
---
# <a name="effectscurrenteffecttype"></a>EFFECTS.currentEffectType

**L'attributo currentEffectType** specifica o recupera il nome del registro della visualizzazione corrente. Questo nome è un ID univoco definito dall'autore della visualizzazione.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

È possibile usare questo attributo in fase di esecuzione per modificare l'effetto attualmente visualizzato. A questo scopo, seguire questa procedura:

1.  Usare **effectCount** per recuperare il conteggio degli effetti registrati.
2.  In un ciclo recuperare il nome di ogni effetto registrato usando **effectType**.
3.  Specificare uno dei nomi recuperati per **currentEffectType per** impostare l'effetto corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTS.effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTS.effectType**](effects-effecttype.md)
</dt> </dl>

 

 





