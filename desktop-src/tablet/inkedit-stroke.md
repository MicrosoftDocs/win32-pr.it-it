---
description: Si verifica quando l'utente disegna un nuovo oggetto IInkStrokeDisp in un oggetto IInkTablet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: Evento InkEdit. Stroke (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759539"
---
# <a name="inkeditstroke-event"></a>Evento InkEdit. Stroke

Si verifica quando l'utente disegna un nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in un oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Tratto* \[ in\]
</dt> <dd>

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

**Variante \_ TRUE** per annullare la raccolta dell'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . **Variante \_ FALSE** per raccogliere l'oggetto **IInkStrokeDisp** e continuare anche con il **tratto** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeStroke.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inchiostrato. h (richiede anche il \_ . c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

