---
description: Si verifica quando l'utente rilascia un pulsante del mouse mentre il mouse è sul controllo InkEdit.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: Evento InkEdit.MouseUp (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483333b246e84d2a9ed6f354198ebce5cd147ddb4fd3ccb5e2834d1802a0b744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712661"
---
# <a name="inkeditmouseup-event"></a>Evento InkEdit.MouseUp

Si verifica quando l'utente rilascia un pulsante del mouse mentre il mouse è sul [controllo InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT MouseUp(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Button* 
</dt> <dd>

Membro [**dell'enumerazione MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) che indica quali pulsanti del mouse sono stati rilasciati.



| Valore                                                                                                                                                            | Significato                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**NO \_ PULSANTE**</dt> </dl>             | Valore predefinito. Non è stato premuto alcun pulsante del mouse. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**SINISTRA \_ PULSANTE**</dt> </dl>       | È stato premuto il pulsante sinistro del mouse. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**RIGHT \_ PULSANTE**</dt> </dl>    | È stato premuto il pulsante destro del mouse. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**MIDDLE \_ PULSANTE**</dt> </dl> | È stato premuto il pulsante centrale del mouse. <br/>  |



 

</dd> <dt>

*MaiuscKey* 
</dt> <dd>

Membro [**dell'enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica quali tasti di modifica vengono premuto al momento dell'evento.



| Valore                                                                                                                                                                                     | Significato                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Spostamento \_ IKM**</dt> </dl>             | Specifica che il tasto MAIUSC è stato usato come modificatore. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Controllo**</dt> </dl> | Specifica che il tasto CTRL è stato usato come modificatore. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ ALT**</dt> </dl>                 | Specifica che il tasto ALT è stato usato come modificatore. <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

Coordinata x corrente, in pixel, del puntatore del mouse.

</dd> <dt>

*yMouse* 
</dt> <dd>

Coordinata y corrente, in pixel, del puntatore del mouse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se viene premuto un pulsante del mouse mentre il puntatore è su un controllo [InkEdit,](inkedit-control-reference.md) il controllo acquisisce il mouse e riceve tutti gli eventi del mouse fino all'ultimo **evento MouseUp** incluso. Ciò implica che le coordinate (x, y) del puntatore del mouse restituite da un evento del mouse potrebbero non essere sempre nell'area interna dell'oggetto che le riceve.

Se i pulsanti del mouse vengono premuti in successione, l'oggetto che acquisisce il mouse dopo la prima pressione riceve tutti gli eventi del mouse fino al rilascio di tutti i pulsanti.

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeMouseUp.

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

[**Enumerazione InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Controllo \[ InkEdit dell'evento MouseDown\]**](inkedit-mousedown.md)
</dt> <dt>

[**Controllo \[ InkEdit dell'evento MouseMove\]**](inkedit-mousemove.md)
</dt> </dl>

 

