---
description: "Evento InkPicture.Stroke: si verifica quando l'utente disegna un nuovo tratto su qualsiasi tablet."
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture.Stroke (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706406ee4f29106fade395a86e9786dd76dec7f51ff2dd77047c2ae395088f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712501"
---
# <a name="inkpicturestroke-event"></a>Evento InkPicture.Stroke

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

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento Stroke.**

</dd> <dt>

*Tratto* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.

</dd> <dt>

*Annulla* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** per annullare la raccolta del tratto. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ ICEStroke DISPID.

**L'evento Stroke** si verifica in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna. A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento. Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.

> [!Note]  
> **L'evento Stroke** si verifica quando l'utente termina di disegnare un tratto, non quando un tratto viene aggiunto alla raccolta [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Quando l'utente inizia per la prima volta a disegnare un tratto, viene aggiunto immediatamente alla raccolta InkStrokes. Tuttavia, **l'evento Stroke** non si verifica fino al completamento del tratto. Di conseguenza, i tratti possono essere presenti nella raccolta InkStrokes che il gestore dell'evento **Stroke** non ha visto.

 

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

[**Controllo InkPicture dell'evento \[ StrokesAdded\]**](inkpicture-strokesadded.md)
</dt> <dt>

[**Controllo InkPicture dell'evento \[ StrokesDeleted\]**](inkpicture-strokesdeleted.md)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

