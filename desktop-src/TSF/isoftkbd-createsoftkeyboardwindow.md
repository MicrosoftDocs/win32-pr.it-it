---
title: Metodo ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: Il metodo ISoftKbd CreateSoftKeyboardWindow crea una finestra di tastiera soft.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Framework servizi di testo Metodo CreateSoftKeyboardWindow
- Framework dei servizi di testo del metodo CreateSoftKeyboardWindow, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518406"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>Metodo ISoftKbd:: CreateSoftKeyboardWindow

Il metodo **ISoftKbd:: CreateSoftKeyboardWindow** crea una finestra di tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hOwner* \[ in\]
</dt> <dd>

Handle della finestra per contenere la tastiera soft.

</dd> <dt>

*\_ Tipo di barra* \[ di titolo in\]
</dt> <dd>

Tipo di barra del titolo per la finestra della tastiera soft. I tipi possibili sono definiti dall'enumerazione del [**\_ tipo di barra**](titlebar-type.md) del titolo.

</dd> <dt>

*XPos* \[ in\]
</dt> <dd>

Posizione x dell'angolo superiore sinistro della finestra della tastiera soft.

</dd> <dt>

*YPos* \[ in\]
</dt> <dd>

Posizione y dell'angolo superiore sinistro della finestra della tastiera soft.

</dd> <dt>

*larghezza* \[ in\]
</dt> <dd>

Larghezza della finestra della tastiera soft.

</dd> <dt>

*altezza* \[ in\]
</dt> <dd>

Altezza della finestra della tastiera soft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono validi.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd::D estroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**tipo di barra di titolo \_**](titlebar-type.md)
</dt> </dl>

 

 





