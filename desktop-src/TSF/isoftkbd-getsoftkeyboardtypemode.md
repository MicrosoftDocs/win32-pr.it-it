---
title: Metodo ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardTypeMode recupera la modalità del tipo per una tastiera soft.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardTypeMode
- Framework dei servizi di testo del metodo GetSoftKeyboardTypeMode, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400207"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>Metodo ISoftKbd:: GetSoftKeyboardTypeMode

Il metodo **ISoftKbd:: GetSoftKeyboardTypeMode** recupera la modalità del tipo per una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpTypeMode* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera la modalità del tipo. I valori possibili sono definiti per l'enumerazione [**TYPEMODE**](typemode.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *lpTypeMode* non è valido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





