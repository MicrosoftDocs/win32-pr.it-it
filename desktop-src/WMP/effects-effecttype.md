---
title: EFFECTs. effectType
description: Il metodo effectType Recupera il nome del registro di sistema della visualizzazione con l'indice del registro di sistema specificato. Questo nome è un ID univoco definito dall'autore della visualizzazione.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328297"
---
# <a name="effectseffecttype"></a>EFFECTs. effectType

Il metodo **effectType** Recupera il nome del registro di sistema della visualizzazione con l'indice del registro di sistema specificato. Questo nome è un ID univoco definito dall'autore della visualizzazione.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice del registro di sistema di una visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa**.

## <a name="remarks"></a>Commenti

Questo metodo è utile per passare da una visualizzazione all'altra nello script. Un'interfaccia utente può visualizzare il set di titoli, ma quando l'utente ne seleziona uno, lo script deve usare **currentEffectType** per cambiare le visualizzazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





