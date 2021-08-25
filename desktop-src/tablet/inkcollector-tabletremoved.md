---
description: 'Evento InkCollector.TabletRemoved: si verifica quando un oggetto IInkTablet viene rimosso dal sistema.'
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Evento InkCollector.TabletRemoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4d3c319a4e67a22c81a74c6b5acceba7bd6f19188042fc68ebe4c7c7c8314e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773521"
---
# <a name="inkcollectortabletremoved-event"></a>Evento InkCollector.TabletRemoved

Si verifica quando [**un oggetto IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene rimosso dal sistema.

## <a name="syntax"></a>Sintassi


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TabletId* \[ Pollici\]
</dt> <dd>

Valore long utilizzato come ID per l'oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) rimosso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICETabletRemoved.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Interfaccia IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




