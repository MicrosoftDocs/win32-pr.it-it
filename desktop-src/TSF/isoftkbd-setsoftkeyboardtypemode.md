---
title: Metodo ISoftKbd SetSoftKeyboardTypeMode (Softkbdc.h)
description: Il metodo ISoftKbd SetSoftKeyboardTypeMode imposta la modalità di tipo per una tastiera soft.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Metodo SetSoftKeyboardTypeMode Framework servizi di testo
- Metodo SetSoftKeyboardTypeMode Framework servizi di testo, interfaccia ISoftKbd
- Interfaccia ISoftKbd Framework servizi di testo metodo SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a43fd160444c2c1d29226aadb898ca60eec6038759452ca8451466337f1b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952487"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a>Metodo ISoftKbd::SetSoftKeyboardTypeMode

Il **metodo ISoftKbd::SetSoftKeyboardTypeMode** imposta la modalità di tipo per una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TypeMode* \[ Pollici\]
</dt> <dd>

Modalità del tipo. I valori possibili sono definiti per [**l'enumerazione TYPEMODE.**](typemode.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro TypeMode* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





