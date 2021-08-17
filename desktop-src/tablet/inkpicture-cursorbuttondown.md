---
description: 'Evento InkPicture.CursorButtonDown: si verifica quando la classe InkCollector rileva un pulsante del cursore verso il basso.'
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Evento InkPicture.CursorButtonDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97305142e14d2200b3ffc98fd83267c515db28a9d4c93c738eb3010bb1b2e371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717340"
---
# <a name="inkpicturecursorbuttondown-event"></a>Evento InkPicture.CursorButtonDown

Si verifica quando [**la classe InkCollector**](inkcollector-class.md) rileva un pulsante del cursore verso il basso.

## <a name="syntax"></a>Sintassi


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorButtonDown.**

</dd> <dt>

*Pulsante* \[ Pollici\]
</dt> <dd>

Pulsante premuto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Un pulsante sulla punta di una penna è verso il basso quando l'utente abbassa la penna al digitalizzatore e inizia a tracciare un tratto. Quando si preme il pulsante, un pulsante su un cane è in giù.

Quando premi il pulsante destro del mouse, ricevi effettivamente due eventi **CursorButtonDown:** uno per il pulsante destro premuto e uno per il pulsante sinistro premuto.

Questo metodo di evento è definito nell'interfaccia di solo invio **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID ICECursorButtonDown.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorDown**](inkpicture-cursordown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




