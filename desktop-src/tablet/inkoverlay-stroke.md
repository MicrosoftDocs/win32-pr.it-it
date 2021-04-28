---
description: "Evento InkOverlay.Stroke: si verifica quando l'utente disegna un nuovo tratto su qualsiasi tablet."
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay.Stroke (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408c44cf47ecfbf3ea0cfd0f8306be61efb0f8e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116849"
---
# <a name="inkoverlaystroke-event"></a>Evento InkOverlay.Stroke

Si verifica quando l'utente disegna un nuovo tratto su qualsiasi tablet.

## <a name="syntax"></a>Sintassi


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento Stroke.**](inkcollector-stroke.md)

</dd> <dt>

*Tratto* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

Specifica se l'evento deve essere annullato. Se **TRUE,** la raccolta del tratto viene annullata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ ICEStroke DISPID.

[**L'evento Stroke**](inkcollector-stroke.md) viene generato in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

> [!Note]  
> [**L'evento Stroke**](inkcollector-stroke.md) viene generato quando l'utente termina di disegnare un tratto, non quando un tratto viene aggiunto alla [raccolta InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Quando l'utente inizia per la prima volta a disegnare un tratto, viene aggiunto immediatamente alla raccolta InkStrokes. Tuttavia, **l'evento Stroke** non viene generato fino al completamento del tratto. Di conseguenza, i tratti possono essere presenti nella raccolta InkStrokes che il gestore dell'evento **Stroke** non ha visto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Raccolta StrokesAdded Event \[ InkStrokes\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**Classe \[ InkOverlay dell'evento StrokesDeleted\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

