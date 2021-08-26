---
description: Si verifica quando un tratto viene aggiunto all'oggetto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp.InkAdded (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a6260660817d38795978371e99b241e3b5b2a88de2d9f2b6d3da678f117b522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939141"
---
# <a name="inkdispinkadded-event"></a>Evento InkDisp.InkAdded

Si verifica quando un tratto viene aggiunto [**all'oggetto InkDisp.**](inkdisp-class.md)

## <a name="syntax"></a>Sintassi


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StrokeIds* \[ Pollici\]
</dt> <dd>

Matrice integer di informazioni sull'ID del tratto per tutti i tratti aggiunti quando si verifica questo evento.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Se usi l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) (dove [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) è uguale a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) è uguale a [**StrokeErase)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)e passi la gomma su un tratto, ottieni la sequenza di eventi seguente:

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Gli eventi **InkAdded** e [**InkDeleted**](inkdisp-inkdeleted.md) aggiuntivi si verificano perché il codice sottostante aggiunge un tratto interno invisibile per tenere traccia della gomma.

Questo metodo di evento è definito \_ nell'interfaccia IInkEvents. \_L'interfaccia IInkEvents implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ di DISPID IEInkAdded.

**L'evento InkAdded** viene generato anche in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Classe \[ InkOverlay della proprietà EditingMode\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**Classe \[ InkOverlay della proprietà EraserMode\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**Evento InkDeleted**](inkdisp-inkdeleted.md)
</dt> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Informazioni di riferimento sul controllo InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

