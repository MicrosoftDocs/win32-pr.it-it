---
description: Si verifica quando l'utente preme un tasto mentre il controllo InkEdit ha lo stato attivo.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Evento InkEdit.KeyDown (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ab1c1b54f9f60d4bd0868f6e093505e21255991502653712a540728394664c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967139"
---
# <a name="inkeditkeydown-event"></a>Evento InkEdit.KeyDown

Si verifica quando l'utente preme un tasto mentre il [controllo InkEdit](inkedit-control-reference.md) ha lo stato attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pKey* 
</dt> <dd>

Codice del tasto virtuale del tasto premuto dall'utente.

</dd> <dt>

*MaiuscKey* 
</dt> <dd>

Membro [**dell'enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica quali tasti di modifica vengono premuto al momento dell'evento.



| Valore                                                                                                                                                                                     | Significato                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Spostamento \_ IKM**</dt> </dl>             | Specifica che il tasto MAIUSC è stato usato come modificatore. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Controllo**</dt> </dl> | Specifica che il tasto CTRL è stato usato come modificatore. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ ALT**</dt> </dl>                 | Specifica che il tasto ALT è stato usato come modificatore. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeKeyDown.

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

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Controllo Input \[ penna evento KeyPressModifica\]**](inkedit-keypress.md)
</dt> <dt>

[**Controllo Input penna \[ evento KeyUpModifica\]**](inkedit-keyup.md)
</dt> </dl>

 

