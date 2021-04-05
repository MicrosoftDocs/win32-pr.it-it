---
description: Si verifica quando viene aggiunto un tratto all'oggetto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049459"
---
# <a name="inkdispinkadded-event"></a>Evento InkDisp. InkAdded

Si verifica quando viene aggiunto un tratto all'oggetto [**InkDisp**](inkdisp-class.md) .

## <a name="syntax"></a>Sintassi


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StrokeIds* \[ in\]
</dt> <dd>

Matrice di interi delle informazioni sull'ID del tratto per tutti i tratti aggiunti quando si verifica questo evento.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Se si utilizza l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) (dove [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) è uguale a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) è uguale a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) e si passa la gomma a un tratto, si ottiene la sequenza di eventi seguente:

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Si verificano gli eventi **InkAdded** e [**InkDeleted**](inkdisp-inkdeleted.md) aggiuntivi perché il codice sottostante aggiunge un tratto invisibile interno per tenere traccia della gomma.

Questo metodo di evento è definito nell' \_ interfaccia IInkEvents. L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IEInkAdded.

L'evento **InkAdded** viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna. A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Classe InkOverlay della proprietà EditingMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**Classe InkOverlay della proprietà EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**Evento InkDeleted**](inkdisp-inkdeleted.md)
</dt> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> <dt>

[Riferimento al controllo InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

