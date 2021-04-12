---
description: Rappresenta la gestione dei mapping dall'input penna alla finestra di visualizzazione. Usare l'oggetto InkRenderer per visualizzare l'input penna in una finestra. È anche possibile usarlo per riposizionare e ridimensionare il tratto.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Classe InkRenderer (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234081"
---
# <a name="inkrenderer-class"></a>Classe InkRenderer

Rappresenta la gestione dei mapping dall'input penna alla finestra di visualizzazione. Usare l'oggetto **InkRenderer** per visualizzare l'input penna in una finestra. È anche possibile usarlo per riposizionare e ridimensionare il tratto.

**InkRenderer** dispone di questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)

### <a name="interfaces"></a>Interfacce

La classe **InkRenderer** definisce queste interfacce.



| Interfaccia        | Descrizione                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Questo oggetto implementa l'interfaccia com **IInkRenderer** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkRenderer** dispone di questi metodi.



| Metodo                                                                     | Descrizione                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Disegna**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Disegna tratti in un contesto di dispositivo.<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Disegna un tratto nel contesto di dispositivo Windows specificato.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Recupera la trasformazione oggetto utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Recupera la trasformazione di visualizzazione utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Converte una posizione nelle coordinate dello spazio input penna in uno spazio in pixel.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Converte una matrice di punti nelle coordinate dello spazio input penna nello spazio pixel.<br/>                                                                          |
| [**Measure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Calcola il rettangolo nel contesto di dispositivo che conterrebbe una raccolta di tratti se sono stati disegnati con l'oggetto **InkRenderer** .<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Calcola il rettangolo nel contesto di dispositivo che conterrebbe un tratto se sono stati disegnati con l'oggetto **InkRenderer** .<br/>                |
| [**Spostare**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Applica una conversione alla trasformazione visualizzazione nelle coordinate dello spazio di input penna.<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Converte una posizione in coordinate pixel nello spazio di input penna.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Converte una matrice di punti in coordinate dello spazio in pixel nello spazio di input penna.<br/>                                                                          |
| [**Ruota**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Applica una rotazione alla trasformazione della vista.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Ridimensiona la trasformazione della vista nella dimensione X e Y.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Imposta la trasformazione oggetto utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Imposta la trasformazione visualizzazione utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                           |



 

## <a name="remarks"></a>Commenti

La stampa viene eseguita anche tramite l'oggetto **InkRenderer** .

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Renderer (proprietà)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**Classe InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

