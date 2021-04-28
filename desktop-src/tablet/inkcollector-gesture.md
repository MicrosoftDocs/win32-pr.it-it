---
description: "Evento InkCollector.Gesture: si verifica quando viene riconosciuto un movimento specifico dell'applicazione."
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: Evento InkCollector.Gesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2fea09060dbb206cd7681bcecfbedbc7a6b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110189"
---
# <a name="inkcollectorgesture-event"></a>Evento InkCollector.Gesture

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

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento Gesture.**

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

**VARIANT \_ TRUE** se questo movimento deve essere annullato. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ ICEGesture DISPID.

Quando la [**proprietà CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) è impostata su [**GestureOnly,**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)il timeout tra quando un utente aggiunge un movimento e quando si verifica l'evento **Gesture** è un valore fisso che non è possibile modificare a livello di codice. Il riconoscimento del movimento è più **veloce in modalità InkAndGesture.**

Per impedire la raccolta di input penna in [**modalità InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Impostare [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) su [**InkAndGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Eliminare il tratto [**nell'evento Stroke.**](inkcollector-stroke.md)
-   Elaborare il movimento **nell'evento Gesture.**

Per evitare il flusso dell'input penna durante la gestione, impostare [**la proprietà DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) su **FALSE.**

Oltre a quando si inserisce l'input penna, **l'evento Gesture** viene generato quando è in modalità di selezione o cancellazione. L'utente è responsabile del rilevamento della modalità di modifica e deve essere a conoscenza della modalità prima di interpretare l'evento.

> [!Note]  
> Per riconoscere i movimenti, è necessario usare un oggetto o un controllo in grado di raccogliere input penna.

 

I movimenti dell'applicazione sono definiti come movimenti supportati all'interno dell'applicazione.

Per il verificarsi di questo evento, l'oggetto o il controllo deve avere interesse per un set di movimenti dell'applicazione. Per impostare gli oggetti o i controlli interessati a un set di movimenti, chiamare il [**metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) dell'oggetto o del controllo.

Per un elenco di movimenti specifici dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Enumerazione InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Uso dei movimenti](using-gestures.md)
</dt> </dl>

 

