---
title: EFFECTS.effectType
description: Il metodo effectType recupera il nome del registro della visualizzazione con l'indice del registro specificato. Questo nome è un ID univoco definito dall'autore della visualizzazione.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTS.effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a452f9218c7004d1078ae6b9e878421a7cad301f3ee913ef6296aaa1c681b736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749233"
---
# <a name="effectseffecttype"></a>EFFECTS.effectType

Il **metodo effectType** recupera il nome del registro della visualizzazione con l'indice del registro specificato. Questo nome è un ID univoco definito dall'autore della visualizzazione.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**long**) contenente l'indice del Registro di sistema di una visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto String.**

## <a name="remarks"></a>Commenti

Questo metodo è utile per passare da una visualizzazione all'altra nello script. Un'interfaccia utente potrebbe visualizzare il set di titoli, ma quando l'utente ne seleziona uno, lo script deve usare **currentEffectType** per cambiare visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





