---
description: Si verifica quando viene riconosciuto un movimento dell'applicazione.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit. Gesture (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232098"
---
# <a name="inkeditgesture-event"></a>Evento InkEdit. Gesture

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

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilizzato per creare questo movimento.

</dd> <dt>

*Tratti* \[ in\]
</dt> <dd>

Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che contiene gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che compongono questo movimento.

</dd> <dt>

*Movimenti* \[ in\]
</dt> <dd>

Matrice di oggetti [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , in ordine di confidenza.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

Indica se la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che costituisce questo movimento deve essere annullata, in modo da non cancellare l'input penna e generare l'evento [**Stroke**](inkedit-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di DISPID \_ IeeGesture.

Un evento di **movimento** viene generato solo se [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) per l'oggetto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) è il primo oggetto **IInkStrokeDisp** dopo l'ultima chiamata al metodo [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o l'ultima generazione del timeout di riconoscimento.

Se l'evento di **movimento** viene annullato, viene generato l'evento [**Stroke**](inkedit-stroke.md) per la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che ha generato l'evento di **movimento** .

Affinché questo evento si verifichi, il controllo [InkEdit](inkedit-control-reference.md) deve sottoscrivere un set di movimenti dell'applicazione. Per impostare l'interesse del controllo InkEdit in un set di movimenti, chiamare il metodo [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .

Per un elenco dei movimenti dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

Il controllo [InkEdit](inkedit-control-reference.md) non riconosce più movimenti del tratto.

Il controllo [InkEdit](inkedit-control-reference.md) sottoscrive i movimenti seguenti.



| Movimento                              | Azione               |
|--------------------------------------|----------------------|
| In basso a sinistra, in basso a sinistra-lungo<br/> | Immettere<br/>     |
| Destra<br/>                     | Space<br/>     |
| Sinistra<br/>                      | Backspace<br/> |
| Up-right, up-right-Long<br/>   | Scheda<br/>       |



 

Per modificare l'azione predefinita per un movimento:

1.  Aggiungere gestori eventi per gli eventi **movimento** e [**tratto**](inkedit-stroke.md) .
2.  Nel gestore eventi **movimento** annullare l'evento di **movimento** per il movimento ed eseguire l'azione alternativa per il movimento.
3.  Nel gestore dell'evento [**Stroke**](inkedit-stroke.md) annullare l'evento **Stroke** per l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che ha generato l'evento di **movimento** annullato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inchiostrato. h (richiede anche il \_ . c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Enumerazione InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Metodo SetGestureStatus ( \[ controllo InkEdit)\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Proprietà RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**\[Controllo InkEdit evento Stroke\]**](inkedit-stroke.md)
</dt> <dt>

[Uso di movimenti](using-gestures.md)
</dt> </dl>

 

