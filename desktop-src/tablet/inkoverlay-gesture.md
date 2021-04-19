---
description: Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: Evento InkOverlay. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3db800db2d1fca9ee1b00620c698a592ac2121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317949"
---
# <a name="inkoverlaygesture-event"></a>InkOverlay. Gesture (evento)

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

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento di [**movimento**](inkcollector-gesture.md) .

</dd> <dt>

*Tratti* \[ in\]
</dt> <dd>

Raccolta [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) restituita dal riconoscimento come movimento.

</dd> <dt>

*Movimenti* \[ in\]
</dt> <dd>

Matrice di oggetti [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , in ordine di confidenza, dal riconoscimento.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

Indica se la raccolta di questo movimento deve essere annullata, ad esempio non cancellare l'input penna e generare l'evento [**Stroke**](inkcollector-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICEGesture.

Quando la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) è impostata su [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), il timeout tra il momento in cui un utente aggiunge un movimento e quando si verifica l'evento di [**movimento**](inkcollector-gesture.md) è un valore fisso che non può essere modificato a livello di codice. Il riconoscimento del movimento è più veloce in modalità **InkAndGesture** .

Per evitare la raccolta di input penna in modalità [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Impostare [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) su [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Eliminare il tratto nell'evento [**Stroke**](inkcollector-stroke.md) .
-   Elaborare il movimento nell'evento di [**movimento**](inkcollector-gesture.md) .

Per impedire il flusso di input penna durante la gestualità, impostare la proprietà [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) su **false**.

Oltre a quando si inserisce l'input penna, l'evento di [**movimento**](inkcollector-gesture.md) viene attivato in modalità selezione o cancellazione. L'utente è responsabile del rilevamento della modalità di modifica e deve tenere presente la modalità prima di interpretare l'evento.

> [!Note]  
> Per riconoscere i movimenti, è necessario utilizzare un oggetto o un controllo in grado di raccogliere input penna.

 

I movimenti dell'applicazione sono definiti come movimenti supportati all'interno dell'applicazione.

Per questo evento, è necessario che l'oggetto o il controllo siano interessati a un set di movimenti dell'applicazione. Per impostare gli oggetti o i controlli interessati da un set di movimenti, chiamare il metodo [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) dell'oggetto o del controllo.

Per un elenco di movimenti specifici dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> <dt>

[**Enumerazione InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Uso di movimenti](using-gestures.md)
</dt> </dl>

 

