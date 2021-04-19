---
title: AmbientAttributes.moveSizeTo
description: Il metodo moveSizeTo sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione. Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- Media Player Windows AmbientAttributes. moveSizeTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326033"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

Il metodo **moveSizeTo** sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione. Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
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

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Number** (**Long**) che specifica il nuovo valore per l'attributo **Width** del controllo.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Number** (**Long**) che specifica il nuovo valore per l'attributo **Height** del controllo.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Numero** (**Long**) che specifica il tempo, in millisecondi, necessario affinché il controllo venga spostato nella nuova posizione.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Valore booleano** che specifica il tipo di movimento creato durante lo spostamento del controllo.



| Valore | Descrizione                                                             |
|-------|-------------------------------------------------------------------------|
| true  | Il movimento è non lineare (movimento scorrevole che accelera e decelera). |
| false | Il movimento è lineare.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il movimento del controllo può essere lineare o non lineare. Movimento lineare significa che il controllo si sposta a una velocità costante nella nuova posizione, avviando e interrompendo bruscamente. Quando si specifica un movimento non lineare, viene creato un movimento scorrevole che accelera da zero all'inizio del movimento e rallenta fino a zero alla fine, arrivando a un punto di interruzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes. Width**](ambientattributes-width.md)
</dt> </dl>

 

 





