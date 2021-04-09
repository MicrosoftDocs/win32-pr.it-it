---
description: Si verifica quando si fa doppio clic sull'oggetto InkCollector o InkOverlay.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878738"
---
# <a name="inkcollectordoubleclick-event"></a>Evento InkCollector. DoubleClick

Si verifica quando si fa doppio clic sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Sintassi


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEDblClick.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> </dl>

 

 




