---
description: "Evento InkCollector.DoubleClick: si verifica quando si fa doppio clic sull'oggetto InkCollector o InkOverlay."
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector.DoubleClick (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51c3fef9ee999bbe2701da64e09a360f07db345
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110209"
---
# <a name="inkcollectordoubleclick-event"></a>Evento InkCollector.DoubleClick

Si verifica quando si fa doppio clic sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)

## <a name="syntax"></a>Sintassi


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** per annullare l'evento per il controllo padre. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEDblClick.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> </dl>

 

 




