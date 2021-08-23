---
description: Indica se un tratto deve essere analizzato come parte di un disegno o come parte della scrittura.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumerazione StrokeType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 4b02a05582d675f04ad4458b1cb21c6d4a1797bacf15baf5d0851804d1a95d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589581"
---
# <a name="stroketype-enumeration"></a>Enumerazione StrokeType

Indica se un tratto deve essere analizzato come parte di un disegno o come parte della scrittura.

## <a name="syntax"></a>Sintassi


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType \_ Unclassified**
</dt> <dd>

Il tratto può essere parte di un disegno o parte della scrittura.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Scrittura di \_ StrokeType**
</dt> <dd>

Il tratto fa parte della scrittura.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Disegno \_ strokeType**
</dt> <dd>

Il tratto fa parte di un disegno.

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio seguente illustra parte di un gestore dell'evento stroke, implementato in modo simile all'esempio [di sink di evento C++.](c---event-sinks-sample.md) Il tratto aggiunto viene controllato per verificare se la parte superiore del relativo rettangolo di selezione è stata disegnata sotto un margine, `drawingMargin` . In tal caso, [**l'oggetto IInkAnalyzer,**](iinkanalyzer.md) , viene impostato per analizzare il tratto come tratto di disegno, anziché `m_spInkAnalyzer` come tratto di scrittura manuale. `CheckHResult`è una funzione che accetta e una stringa e genera un'eccezione creata con `HRESULT` la stringa se non è `HRESULT` **SUCCESS.**


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




