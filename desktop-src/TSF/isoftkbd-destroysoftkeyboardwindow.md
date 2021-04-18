---
title: Metodo ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: Il metodo ISoftKbd DestroySoftKeyboardWindow Elimina una finestra della tastiera soft.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Framework servizi di testo Metodo DestroySoftKeyboardWindow
- Framework dei servizi di testo del metodo DestroySoftKeyboardWindow, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301686"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a>ISoftKbd::D Metodo estroySoftKeyboardWindow

Il metodo **ISoftKbd::D estroysoftkeyboardwindow** Elimina una finestra della tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                | Descrizione                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo rimuove una finestra di tastiera soft creata in precedenza con una chiamata a [**ISoftKbd:: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).

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

[**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





