---
title: AmbientAttributes.slideTo
description: Il metodo slideTo sposta il controllo in una nuova posizione. Il controllo si sposta in modo non lineare nel periodo di tempo specificato.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes.slideTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f199a2786adbd63313c3f500d589f9f51e2b8ca2fa8120a8fdf75021041115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469911"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

Il **metodo slideTo** sposta il controllo in una nuova posizione. Il controllo si sposta in modo non lineare nel periodo di tempo specificato.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per **l'attributo** sinistro del controllo.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per **l'attributo** principale del controllo.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Numero** (**long**) che specifica il tempo, in millisecondi, necessario per lo spostamento del controllo nella nuova posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è diverso da **moveTo,** che crea un movimento lineare quando si sposta il controllo. Il movimento non lineare creato da questo metodo è un movimento scorrevole che accelera da una velocità pari a zero all'inizio del movimento e decelera di nuovo a zero alla fine, fino a un arresto uniforme.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





