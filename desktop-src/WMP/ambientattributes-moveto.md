---
title: AmbientAttributes.moveTo
description: Il metodo moveTo sposta il controllo in una nuova posizione a una velocità lineare.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes.moveTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf05beedad4fe4abb839e957519384b58102253cd0ab6a292d629df23a7bef98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055049"
---
# <a name="ambientattributesmoveto"></a>AmbientAttributes.moveTo

Il **metodo moveTo** sposta il controllo in una nuova posizione a una velocità lineare.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per l'attributo **a** sinistra del controllo.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per **l'attributo** top del controllo.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*Tempo*
</dt> <dd>

**Numero** (**long**) che specifica il tempo, in millisecondi, necessario per il passaggio del controllo alla nuova posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è utile per gli elementi **SUBVIEW** animati, ad esempio se l'utente fa clic su un vassoio e i controlli slittano verso il basso.

Questo metodo crea un movimento lineare quando si sposta il controllo. Questo comportamento è diverso **da slideTo,** che crea un movimento non lineare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.slideTo**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





