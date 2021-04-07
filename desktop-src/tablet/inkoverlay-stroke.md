---
description: Si verifica quando l'utente disegna un nuovo tratto su un tablet.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759530"
---
# <a name="inkoverlaystroke-event"></a>InkOverlay. Stroke (evento)

Si verifica quando l'utente disegna un nuovo tratto su un tablet.

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

*Cursore* \[ in\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**Stroke**](inkcollector-stroke.md) .

</dd> <dt>

*Tratto* \[ in\]
</dt> <dd>

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.

</dd> <dt>

*Annulla* \[ in uscita\]
</dt> <dd>

Specifica se l'evento deve essere annullato. Se **true**, la raccolta del tratto viene annullata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICEStroke.

L'evento [**Stroke**](inkcollector-stroke.md) viene generato in modalità Select o Erase, non solo quando si inserisce l'input penna. A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.

> [!Note]  
> L'evento [**Stroke**](inkcollector-stroke.md) viene generato quando l'utente completa il disegno di un tratto, non quando un tratto viene aggiunto alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Quando l'utente inizia per la prima volta a disegnare un tratto, viene aggiunto immediatamente alla raccolta InkStrokes. Tuttavia, l'evento **Stroke** non viene attivato fino al completamento del tratto. Di conseguenza, i tratti possono esistere nella raccolta InkStrokes che il gestore dell'evento **Stroke** non ha rilevato.

 

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

[**\[Raccolta InkStrokes evento StrokesAdded\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**Classe InkOverlay dell'evento StrokesDeleted \[\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

