---
description: Si verifica quando l'utente sposta il mouse mentre il mouse è sul controllo InkEdit.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: Evento InkEdit.MouseMove (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 601bcaa4c5bc3379c207302c28e5eb17d44b2b184ce42452d5b78b6079d88ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939111"
---
# <a name="inkeditmousemove-event"></a>Evento InkEdit.MouseMove

Si verifica quando l'utente sposta il mouse mentre il mouse è sul [controllo InkEdit.](inkedit-control-reference.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT MouseMove(
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

Membro [**dell'enumerazione MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) che indica quali pulsanti del mouse sono visualizzati.



| Valore                                                                                                                                                            | Significato                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**NO \_ PULSANTE**</dt> </dl>             | Valore predefinito. Non è stato premuto alcun pulsante del mouse. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**LEFT \_ PULSANTE**</dt> </dl>       | È stato premuto il pulsante sinistro del mouse. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**RIGHT \_ PULSANTE**</dt> </dl>    | È stato premuto il pulsante destro del mouse. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**MIDDLE \_ PULSANTE**</dt> </dl> | È stato premuto il pulsante centrale del mouse. <br/>  |



 

</dd> <dt>

*MaiuscKey* 
</dt> <dd>

Membro [**dell'enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica quali tasti di modifica vengono pre-modificati al momento dell'evento.



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

Se l'evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se viene premuto un pulsante del mouse mentre il puntatore è posizionato su un controllo [InkEdit,](inkedit-control-reference.md) tale controllo acquisisce il mouse e riceve tutti gli eventi del mouse fino all'ultimo [**evento MouseUp**](inkedit-mouseup.md) incluso. Ciò implica che le coordinate del puntatore del mouse (x, y) restituite da un evento del mouse potrebbero non essere sempre nell'area interna dell'oggetto che le riceve.

Se i pulsanti del mouse vengono premuti in successione, l'oggetto che acquisisce il mouse dopo la prima pressione riceve tutti gli eventi del mouse finché non vengono rilasciati tutti i pulsanti.

**L'evento MouseMove** viene generato continuamente quando il puntatore del mouse si sposta tra gli oggetti. A meno che un altro oggetto non abbia acquisito il mouse, un controllo [InkEdit](inkedit-control-reference.md) riconosce un **evento MouseMove** ogni volta che la posizione del mouse si trova all'interno dei bordi.

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ di DISPID IeeeMouseMove.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche \_ i.c con input penna)</dt> </dl> |
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

[**Controllo \[ InkEdit dell'evento MouseUp\]**](inkedit-mouseup.md)
</dt> </dl>

 

