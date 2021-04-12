---
description: Si verifica quando l'utente rilascia un pulsante del mouse mentre il mouse si trova sul controllo InkEdit.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: Evento InkEdit. MouseUp (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c331ec5dd0dd6a39ec956eda6980ee02cddd298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233558"
---
# <a name="inkeditmouseup-event"></a>Evento InkEdit. MouseUp

Si verifica quando l'utente rilascia un pulsante del mouse mentre il mouse si trova sul controllo [InkEdit](inkedit-control-reference.md) .

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

Membro dell'enumerazione [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) che indica quali pulsanti del mouse sono stati rilasciati.



| Valore                                                                                                                                                            | Significato                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**No \_ PULSANTE**</dt> </dl>             | Valore predefinito. Non è stato premuto alcun pulsante del mouse. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>A **sinistra \_ PULSANTE**</dt> </dl>       | È stato premuto il pulsante sinistro del mouse. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>A **destra \_ PULSANTE**</dt> </dl>    | È stato premuto il pulsante destro del mouse. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>Al **centro \_ PULSANTE**</dt> </dl> | È stato premuto il pulsante centrale del mouse. <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Membro dell'enumerazione [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica i tasti di modifica che vengono depressi al momento dell'evento.



| Valore                                                                                                                                                                                     | Significato                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Specifica che il tasto MAIUSC è stato utilizzato come modificatore. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Controllo** di</dt> </dl> | Specifica che il tasto CTRL è stato utilizzato come modificatore. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Specifica che il tasto ALT è stato utilizzato come modificatore. <br/>   |



 

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

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se viene premuto un pulsante del mouse mentre il puntatore è posizionato su un controllo [InkEdit](inkedit-control-reference.md) , il controllo acquisisce il mouse e riceve tutti gli eventi del mouse fino a includere l'ultimo evento **MouseUp** . Ciò implica che le coordinate del puntatore del mouse (x, y) restituite da un evento del mouse potrebbero non trovarsi sempre nell'area interna dell'oggetto che li riceve.

Se i pulsanti del mouse vengono premuti in successione, l'oggetto che acquisisce il mouse dopo la prima pressione riceve tutti gli eventi del mouse fino a quando non vengono rilasciati tutti i pulsanti.

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeMouseUp.

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

[**Enumerazione InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**\[Controllo InkEdit evento MouseDown\]**](inkedit-mousedown.md)
</dt> <dt>

[**\[Controllo InkEdit evento MouseMove\]**](inkedit-mousemove.md)
</dt> </dl>

 

