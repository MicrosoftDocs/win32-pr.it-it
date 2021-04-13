---
title: Metodo ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: Il metodo ISoftKbd SelectSoftKeyboard seleziona la tastiera soft specificata.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Framework servizi di testo Metodo SelectSoftKeyboard
- Framework dei servizi di testo del metodo SelectSoftKeyboard, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518514"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>Metodo ISoftKbd:: SelectSoftKeyboard

Il metodo **ISoftKbd:: SelectSoftKeyboard** seleziona la tastiera soft specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwKeyboardId* \[ in\]
</dt> <dd>

Identificatore della tastiera soft da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *dwKeyboardId* non è valido.<br/> |



 

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
</dt> </dl>

 

 





