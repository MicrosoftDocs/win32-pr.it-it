---
description: "Evento InkPicture.Gesture: si verifica quando viene riconosciuto un movimento specifico dell'applicazione."
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture.Gesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c0307397fc5a197666894d40adce6f4a579e22d896df8df645b053580ee94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451068"
---
# <a name="inkpicturegesture-event"></a>Evento InkPicture.Gesture

Si verifica quando viene riconosciuto un movimento *specifico dell'applicazione.*

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

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento Gesture.**

</dd> <dt>

*Tratti* \[ Pollici\]
</dt> <dd>

Raccolta [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) restituita dal riconoscitore come movimento.

</dd> <dt>

*Movimenti* \[ Pollici\]
</dt> <dd>

Matrice di [**oggetti IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in ordine di attendibilità, dal sistema di riconoscimento.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** se questo evento deve essere annullato, ad esempio per non cancellare l'input penna e per genera [**l'evento Stroke.**](inkpicture-stroke.md) In caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ ICEGesture DISPID.

Quando la [**proprietà CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) è impostata su [**GestureOnly,**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)il timeout tra quando un utente aggiunge un movimento e quando si verifica l'evento **Gesture** è un valore fisso che non è possibile modificare a livello di codice. Il riconoscimento dei movimenti è più **veloce in modalità InkAndGesture.**

Per impedire la raccolta di input penna in [**modalità InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Impostare [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) su [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Eliminare il tratto [**nell'evento Stroke.**](inkpicture-stroke.md)
-   Elaborare il movimento **nell'evento Gesture.**

Per evitare il flusso dell'input penna durante la gestione, impostare [**la proprietà DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) su **FALSE.**

Oltre a quando si inserisce l'input penna, **l'evento Gesture** viene generato quando è in modalità di selezione o cancellazione. L'utente è responsabile del rilevamento della modalità di modifica e deve essere a conoscenza della modalità prima di interpretare l'evento.

> [!Note]  
> Per riconoscere i movimenti, è necessario usare un oggetto o un controllo in grado di raccogliere input penna.

 

I movimenti dell'applicazione sono definiti come movimenti supportati all'interno dell'applicazione.

Per il verificarsi di questo evento, l'oggetto o il controllo deve avere interesse per un set di movimenti dell'applicazione. Per impostare gli oggetti o i controlli interessati a un set di movimenti, chiamare il [**metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) dell'oggetto o del controllo.

Per un elenco di movimenti specifici dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Enumerazione InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[Uso dei movimenti](using-gestures.md)
</dt> </dl>

 

