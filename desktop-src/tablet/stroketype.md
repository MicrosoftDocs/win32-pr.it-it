---
description: Indica se un tratto deve essere analizzato come parte di un disegno o come parte della scrittura.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumerazione StrokeType (IACom. h)
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
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232704"
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

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType non \_ Classificato**
</dt> <dd>

Il tratto può essere parte di un disegno o parte della scrittura.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**\_Scrittura StrokeType**
</dt> <dd>

Il tratto fa parte della scrittura.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**\_Disegno StrokeType**
</dt> <dd>

Il tratto fa parte di un disegno.

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata una parte di un gestore eventi Stroke, implementata in modo simile all' [esempio di sink di eventi C++](c---event-sinks-sample.md). Il tratto aggiunto viene controllato per verificare se la parte superiore del riquadro è stata disegnata al di sotto di un margine `drawingMargin` . In tal caso, [](iinkanalyzer.md) l'oggetto IInkAnalyzer `m_spInkAnalyzer` è impostato per analizzare il tratto come tratto di disegno, anziché come tratto di grafia. `CheckHResult` è una funzione che accetta un oggetto `HRESULT` e una stringa e genera un'eccezione creata con la stringa se `HRESULT` non ha **esito positivo**.


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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




