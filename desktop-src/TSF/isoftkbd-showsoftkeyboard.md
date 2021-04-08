---
title: Metodo ISoftKbd ShowSoftKeyboard (Softkbdc. h)
description: Il metodo ISoftKbd ShowSoftKeyboard Visualizza una tastiera soft.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Framework servizi di testo Metodo ShowSoftKeyboard
- Framework dei servizi di testo del metodo ShowSoftKeyboard, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo ShowSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047818"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a>Metodo ISoftKbd:: ShowSoftKeyboard

Il metodo **ISoftKbd:: ShowSoftKeyboard** Visualizza una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iShow* \[ in\]
</dt> <dd>

Integer che indica il tipo di tastiera soft da visualizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                | Descrizione                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

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

 

 





