---
description: Si verifica quando viene riconosciuto un movimento dell'applicazione.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit.Gesture (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a718106f4485682a1b6267f942ec3ef0f5a9fb670449e1f6023d86a5b03af56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032079"
---
# <a name="inkeditgesture-event"></a>Evento InkEdit.Gesture

Si verifica quando viene riconosciuto un movimento dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Gesture(
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

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare questo movimento.

</dd> <dt>

*Tratti* \[ Pollici\]
</dt> <dd>

Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che contiene gli [**oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che costituiscono questo movimento.

</dd> <dt>

*Movimenti* \[ Pollici\]
</dt> <dd>

Matrice di [**oggetti IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in ordine di attendibilità.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

Indica se [la raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che costituisce questo movimento deve essere annullata, in modo da non cancellare l'input penna e per creare l'evento [**Stroke.**](inkedit-stroke.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di DISPID \_ IeeGesture.

Un evento **Gesture** viene generato solo se [**L'oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) per [**l'oggetto IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) è il primo **oggetto IInkStrokeDisp** dopo l'ultima chiamata al metodo [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o l'ultima attivazione del timeout di riconoscimento.

Se **l'evento Gesture** viene annullato, viene generato [**l'evento Stroke**](inkedit-stroke.md) per la [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che ha generato **l'evento Gesture.**

Per il verificarsi di questo evento, il [controllo InkEdit](inkedit-control-reference.md) deve sottoscrivere un set di movimenti dell'applicazione. Per impostare l'interesse del controllo InkEdit in un set di movimenti, chiamare il [**metodo SetGestureStatus.**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)

Per un elenco dei movimenti dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

Il [controllo InkEdit](inkedit-control-reference.md) non riconosce più movimenti del tratto.

Il [controllo InkEdit](inkedit-control-reference.md) sottoscrive i movimenti seguenti.



| Movimento                              | Azione               |
|--------------------------------------|----------------------|
| In basso a sinistra, lungo verso il basso a sinistra<br/> | Immettere<br/>     |
| Destra<br/>                     | Space<br/>     |
| Sinistra<br/>                      | Backspace<br/> |
| Up-right, Up-right-long<br/>   | Scheda<br/>       |



 

Per modificare l'azione predefinita per un movimento:

1.  Aggiungere gestori eventi per gli **eventi Gesture** [**e Stroke.**](inkedit-stroke.md)
2.  Nel gestore **dell'evento Gesture** annullare l'evento **Gesture** per il movimento ed eseguire l'azione alternativa per il movimento.
3.  Nel gestore [**dell'evento Stroke**](inkedit-stroke.md) annullare l'evento **Stroke** per [**l'oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che ha generato l'evento **Gesture** annullato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche \_ l'input penna i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Enumerazione InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Controllo InkEdit del metodo SetGestureStatus \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Proprietà RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**Controllo \[ InkEdit dell'evento Stroke\]**](inkedit-stroke.md)
</dt> <dt>

[Uso dei movimenti](using-gestures.md)
</dt> </dl>

 

