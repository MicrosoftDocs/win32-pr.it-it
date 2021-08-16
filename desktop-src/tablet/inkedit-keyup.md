---
description: Si verifica quando l'utente rilascia un tasto mentre il controllo InkEdit ha lo stato attivo.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Evento InkEdit.KeyUp (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ac908202a22fc1f564c3f21da4cc3cce2e79e2f093ec93b65ff56066f94510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220756"
---
# <a name="inkeditkeyup-event"></a>Evento InkEdit.KeyUp

Si verifica quando l'utente rilascia un tasto mentre il [controllo InkEdit](inkedit-control-reference.md) ha lo stato attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT KeyUp(
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

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeKeyUp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche input \_ penna i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Enumerazione InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Controllo \[ InkEdit dell'evento KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**Controllo Input \[ penna evento KeyPressModifica\]**](inkedit-keypress.md)
</dt> </dl>

 

