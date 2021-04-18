---
title: AmbientAttributes. MoveTo
description: Il metodo MoveTo sposta il controllo in una nuova posizione a una velocità lineare.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Media Player di Windows AmbientAttributes. MoveTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327170"
---
# <a name="ambientattributesmoveto"></a>AmbientAttributes. MoveTo

Il metodo **MoveTo** sposta il controllo in una nuova posizione a una velocità lineare.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**Number** (**Long**) che specifica il nuovo valore per l'attributo **Left** del controllo.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**Number** (**Long**) che specifica il nuovo valore per l'attributo **Top** del controllo.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*tempo*
</dt> <dd>

**Numero** (**Long**) che specifica il tempo, in millisecondi, necessario affinché il controllo venga spostato nella nuova posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è utile per gli elementi di **Sottovisualizzazione** animati (ad esempio, se l'utente fa clic su un vassoio e i controlli scorrono verso il basso).

Questo metodo crea un movimento lineare durante lo spostamento del controllo. Questo comportamento è diverso da **slideTo**, che consente di creare un movimento non lineare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.slideTo**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





