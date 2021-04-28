---
description: "Evento InkOverlay.DoubleClick: si verifica quando si fa doppio clic sull'oggetto InkCollector o InkOverlay."
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Evento InkOverlay.DoubleClick (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086829"
---
# <a name="inkoverlaydoubleclick-event"></a>Evento InkOverlay.DoubleClick

Si verifica quando si fa doppio clic [**sull'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)

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

Indica se l'evento deve essere annullato per il controllo padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEDblClick.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> </dl>

 

 




