---
description: Rappresenta gli attributi applicati all'input penna quando viene disegnata.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Classe InkDrawingAttributes (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347906"
---
# <a name="inkdrawingattributes-class"></a>Classe InkDrawingAttributes

Rappresenta gli attributi applicati all'input penna quando viene disegnata.

**InkDrawingAttributes** dispone di questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="interfaces"></a>Interfacce

La classe **InkDrawingAttributes** definisce queste interfacce.



| Interfaccia                 | Descrizione                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | Questo oggetto implementa l'interfaccia com **IInkDrawingAttributes** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkDrawingAttributes** dispone di questi metodi.



| Metodo                         | Descrizione                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Crea un oggetto [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** o [**InkRecognizerContext**](inkrecognizercontext-class.md) duplicato.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **InkDrawingAttributes** dispone di queste proprietà.



| Proprietà                                                                           | Tipo di accesso           | Descrizione                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Antialias**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il valore che specifica se i colori di primo piano e di sfondo lungo il bordo dell'input penna vengono combinati per aumentare la smussatura di un tratto di input penna.<br/> |
| [**Colore**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta il colore dell'input penna creato con questo oggetto **InkDrawingAttributes** .<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Sola lettura<br/>  | Ottiene la raccolta di dati definiti dall'applicazione archiviati nell'oggetto **InkDrawingAttributes** .<br/>                                                                |
| [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta il valore che specifica se viene eseguito il rendering dell'input penna come una serie di curve anziché come linee tra i punti di esempio della penna.<br/>                                    |
| [**Altezza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta l'altezza della penna quando si disegna l'input penna con questo oggetto **InkDrawingAttributes** .<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta il valore che specifica se l'input penna automatico diventa più ampio con una maggiore pressione della punta della penna sulla superficie del tablet.<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta la punta della penna da usare (palla o rettangolo) quando si disegna l'input penna con questo oggetto **InkDrawingAttributes** .<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta il modo in cui il colore della penna interagisce con i colori di sfondo esistenti sullo schermo quando viene disegnato l'input penna.<br/>                                                    |
| [**Trasparenza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta il valore di trasparenza dell'input penna. I valori sono compresi tra zero (completamente opaco) e 255 (completamente trasparente).<br/>                                               |
| [**Larghezza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta la larghezza della penna durante il disegno dell'input penna con questo oggetto **InkDrawingAttributes** .<br/>                                                                         |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

Questi attributi di disegno possono essere associati a un tratto o a un cursore e specificare impostazioni quali il colore, la larghezza e la trasparenza.

Per specificare gli attributi di disegno di un tratto, utilizzare la proprietà [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) dell'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Per specificare gli attributi di disegno di tutti i tratti all'interno di una raccolta di tratti, chiamare il metodo [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Ogni oggetto [**InkCollector**](inkcollector-class.md) , oggetto [**InkOverlay**](inkoverlay-class.md) e controllo [InkPicture](inkpicture-control-reference.md) può specificare un set diverso di attributi di disegno per lo stesso cursore. Utilizzare la proprietà [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) per ottenere o impostare gli attributi di disegno di un cursore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DrawingAttributes (proprietà)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes (proprietà)**
</dt> <dt>

**DrawingAttributes (proprietà)**
</dt> <dt>

[**Proprietà DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**Proprietà DefaultDrawingAttributes**
</dt> <dt>

**Proprietà DefaultDrawingAttributes**
</dt> <dt>

[**Metodo ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

