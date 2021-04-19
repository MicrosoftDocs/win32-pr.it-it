---
title: AmbientAttributes.slideTo
description: Il metodo slideTo sposta il controllo in una nuova posizione. Il controllo viene spostato in modo non lineare nel periodo di tempo specificato.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Media Player Windows AmbientAttributes. slideTo
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332148"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

Il metodo **slideTo** sposta il controllo in una nuova posizione. Il controllo viene spostato in modo non lineare nel periodo di tempo specificato.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Number** (**Long**) che specifica il nuovo valore per l'attributo **Left** del controllo.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Number** (**Long**) che specifica il nuovo valore per l'attributo **Top** del controllo.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Numero** (**Long**) che specifica il tempo, in millisecondi, necessario affinché il controllo venga spostato nella nuova posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è diverso da **MoveTo**, che crea un movimento lineare durante lo spostamento del controllo. Il movimento non lineare creato da questo metodo è un movimento scorrevole che accelera da una velocità pari a zero all'inizio del movimento e rallenta fino a zero alla fine, arrivando a un punto di arresto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes. MoveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





