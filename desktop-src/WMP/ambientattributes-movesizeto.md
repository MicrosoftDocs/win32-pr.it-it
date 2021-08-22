---
title: AmbientAttributes.moveSizeTo
description: Il metodo moveSizeTo sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione. Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes.moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936a6696dfcc99c5a181906eb970f84c7019af7905c466f09e820044f6220271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469951"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

Il **metodo moveSizeTo** sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione. Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per l'attributo **a** sinistra del controllo.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per **l'attributo** top del controllo.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per l'attributo **width** del controllo.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Numero** (**long**) che specifica il nuovo valore per l'attributo **height** del controllo.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Numero** (**long**) che specifica il tempo, in millisecondi, necessario per il passaggio del controllo alla nuova posizione.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Valore** booleano che specifica il tipo di movimento creato durante lo spostamento del controllo.



| Valore | Descrizione                                                             |
|-------|-------------------------------------------------------------------------|
| true  | Il movimento è non lineare (movimento scorrevole che accelera e decelera). |
| false | Il movimento è lineare.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il movimento del controllo può essere lineare o non lineare. Il movimento lineare indica che il controllo si sposta a una velocità costante nella nuova posizione, iniziando e arrestando improvvisamente. Quando si specifica un movimento non lineare, viene creato un movimento scorrevole che accelera da zero all'inizio del movimento e decelera di nuovo a zero alla fine, fino a un arresto uniforme.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes.width**](ambientattributes-width.md)
</dt> </dl>

 

 





