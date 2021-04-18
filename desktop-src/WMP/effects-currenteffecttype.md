---
title: EFFECTs. currentEffectType
description: L'attributo currentEffectType specifica o Recupera il nome del registro di sistema della visualizzazione corrente. Questo nome è un ID univoco definito dall'autore della visualizzazione.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325847"
---
# <a name="effectscurrenteffecttype"></a>EFFECTs. currentEffectType

L'attributo **currentEffectType** specifica o Recupera il nome del registro di sistema della visualizzazione corrente. Questo nome è un ID univoco definito dall'autore della visualizzazione.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

È possibile usare questo attributo in fase di esecuzione per modificare l'effetto attualmente visualizzato. A questo scopo, seguire questa procedura:

1.  Usare **effectCount** per recuperare il conteggio degli effetti registrati.
2.  In un ciclo recuperare il nome di ogni effetto registrato utilizzando **effectType**.
3.  Specificare uno dei nomi recuperati per **currentEffectType** per impostare l'effetto corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTs. effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTs. effectType**](effects-effecttype.md)
</dt> </dl>

 

 





