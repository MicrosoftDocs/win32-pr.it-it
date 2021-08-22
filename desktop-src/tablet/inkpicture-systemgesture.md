---
description: 'InkPicture.Sysevento temGesture: si verifica quando viene riconosciuto un movimento di sistema.'
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.SystemGesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11567b94360c8fa2bf736d295bf828ebc636bb0bee7a21acb4cc063c22780352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966950"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture.SystemGesture

Si verifica quando viene riconosciuto un movimento di sistema.

## <a name="syntax"></a>Sintassi


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cursore* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento SystemGesture.**

</dd> <dt>

*ID* \[ in\]
</dt> <dd>

Valore del movimento di sistema.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Coordinata x della posizione del movimento.

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

Coordinata y della posizione del movimento.

</dd> <dt>

*Modificatore* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*Carattere* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> <dt>

*CursorMode* \[ Pollici\]
</dt> <dd>

Valore che indica se [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma. 1 è per la modalità normale e 2 per la modalità gomma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I movimenti di sistema forniscono informazioni [**sull'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento. Forniscono anche collegamenti a combinazioni di eventi del mouse e sono modi per rilevare gli eventi del mouse con un impatto minore sulle prestazioni.

Ad esempio, anziché cercare una coppia di eventi [**MouseUp Event \[ InkPicture Control \]**](inkpicture-mouseup.md)MouseDown Event / [**\[ InkPicture Control \]**](inkpicture-mousedown.md) di eventi senza altri eventi del mouse che si verificano tra, è possibile cercare i movimenti di sistema Tap o RightTap.

Come altro esempio, invece di ascoltare gli eventi di controllo [**\[ InkPicture \]**](inkpicture-mousedown.md)Event MouseMove Event / [**\[ InkPicture Control \]**](inkpicture-mousemove.md) dell'evento MouseDown e ricevere numerosi messaggi di controllo InkPicture **\[ \]** dell'evento MouseMove, è possibile controllare i movimenti di sistema Drag o RightDrag purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse. In questo modo è possibile ricevere un solo messaggio anziché numerosi messaggi di controllo **\[ InkPicture \]** dell'evento MouseMove.

Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Per altre informazioni sui movimenti di sistema, vedere [Uso di movimenti e](using-gestures.md) input dei comandi nel Tablet [PC.](/previous-versions//dd314533(v=vs.85))

Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ ICESystemGesture DISPID.

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

[**Enumerazione InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Uso dei movimenti](using-gestures.md)
</dt> </dl>

 

