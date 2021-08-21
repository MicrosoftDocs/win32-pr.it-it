---
description: Rappresenta la gestione dei mapping dall'input penna alla finestra di visualizzazione. Usare l'oggetto InkRenderer per visualizzare l'input penna in una finestra. È anche possibile usarlo per riposizionare e ridimensionare il tratto.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Classe InkRenderer (Msinkaut.h)
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
ms.openlocfilehash: f03b65a1ce009313b996fc7bede03f8c7425ff589fd29506c243f3161a851583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938721"
---
# <a name="inkrenderer-class"></a>Classe InkRenderer

Rappresenta la gestione dei mapping dall'input penna alla finestra di visualizzazione. Usare **l'oggetto InkRenderer** per visualizzare l'input penna in una finestra. È anche possibile usarlo per riposizionare e ridimensionare il tratto.

**InkRenderer** ha questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)

### <a name="interfaces"></a>Interfacce

La **classe InkRenderer** definisce queste interfacce.



| Interfaccia        | Descrizione                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | Questo oggetto implementa **l'interfaccia COM IInkRenderer.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe InkRenderer** include questi metodi.



| Metodo                                                                     | Descrizione                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Disegna**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | Disegna tratti in un contesto di dispositivo.<br/>                                                                                                            |
| [**Sequenza di disegno**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | Disegna un tratto nel contesto di dispositivo windows specificato.<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | Recupera la trasformazione dell'oggetto utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | Recupera la trasformazione di visualizzazione utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | Converte una posizione nelle coordinate dello spazio input penna in modo che sia nello spazio pixel.<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | Converte una matrice di punti nelle coordinate dello spazio input penna in spazio pixel.<br/>                                                                          |
| [**Misura**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | Calcola il rettangolo nel contesto di dispositivo che conterrà una raccolta di tratti se fossero stati disegnati con **l'oggetto InkRenderer.**<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | Calcola il rettangolo nel contesto di dispositivo che conterrà un tratto se fossero stati disegnati con **l'oggetto InkRenderer.**<br/>                |
| [**Sposta**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | Applica una traslazione alla trasformazione della visualizzazione in coordinate dello spazio input penna.<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | Converte una posizione in coordinate pixel nello spazio input penna.<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | Converte una matrice di punti nelle coordinate dello spazio pixel in spazio input penna.<br/>                                                                          |
| [**Ruota**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | Applica una rotazione alla trasformazione della visualizzazione.<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | Ridimensiona la trasformazione della vista nella dimensione X e Y.<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | Imposta la trasformazione dell'oggetto utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | Imposta la trasformazione di visualizzazione utilizzata per eseguire il rendering dell'input penna.<br/>                                                                                           |



 

## <a name="remarks"></a>Commenti

La stampa viene eseguita anche tramite **l'oggetto InkRenderer.**

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**Classe InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

