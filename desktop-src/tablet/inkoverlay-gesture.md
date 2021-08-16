---
description: "Evento InkOverlay.Gesture: si verifica quando viene riconosciuto un movimento specifico dell'applicazione."
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: Evento InkOverlay.Gesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01689465e9951a5b8cd6548cabb0be4a0bde32c7cf46c2ea4c71b3bb38151eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219312"
---
# <a name="inkoverlaygesture-event"></a>Evento InkOverlay.Gesture

Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento Gesture.**](inkcollector-gesture.md)

</dd> <dt>

*Tratti* \[ Pollici\]
</dt> <dd>

Raccolta [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) restituita dal riconoscimento come movimento.

</dd> <dt>

*Movimenti* \[ Pollici\]
</dt> <dd>

Matrice di [**oggetti IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in ordine di confidenza, dal sistema di riconoscimento.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

Indica se la raccolta di questo movimento deve essere annullata, ad esempio per non cancellare l'input penna e per la generazione [**dell'evento Stroke.**](inkcollector-stroke.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ ICEGesture DISPID.

Quando la [**proprietà CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) è impostata su [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), il timeout tra quando un utente aggiunge un movimento e quando si verifica l'evento [**Gesture**](inkcollector-gesture.md) è un valore fisso che non è possibile modificare a livello di codice. Il riconoscimento del movimento è più **veloce in modalità InkAndGesture.**

Per impedire la raccolta di input penna in [**modalità InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Impostare [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) su [**InkAndGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Eliminare il tratto [**nell'evento Stroke.**](inkcollector-stroke.md)
-   Elaborare il movimento [**nell'evento Gesture.**](inkcollector-gesture.md)

Per impedire il flusso dell'input penna durante l'inserimento, [**impostare la proprietà DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) su **FALSE.**

Oltre a quando si inserisce l'input penna, l'evento [**Gesture**](inkcollector-gesture.md) viene generato in modalità di selezione o cancellazione. L'utente è responsabile del rilevamento della modalità di modifica e deve essere a conoscenza della modalità prima di interpretare l'evento.

> [!Note]  
> Per riconoscere i movimenti, è necessario usare un oggetto o un controllo in grado di raccogliere input penna.

 

I movimenti dell'applicazione sono definiti come movimenti supportati all'interno dell'applicazione.

Perché questo evento si verifichi, l'oggetto o il controllo deve essere interessato a un set di movimenti dell'applicazione. Per impostare l'interesse degli oggetti o dei controlli in un set di movimenti, chiamare il [**metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) dell'oggetto o del controllo.

Per un elenco di movimenti specifici dell'applicazione, vedere il [**tipo di enumerazione InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumerazione InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Uso dei movimenti](using-gestures.md)
</dt> </dl>

 

