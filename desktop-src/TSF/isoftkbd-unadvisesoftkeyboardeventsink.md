---
title: Metodo ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: Il metodo ISoftKbd UnadviseSoftKeyboardEventSink rimuove un sink di evento della tastiera soft.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Framework servizi di testo Metodo UnadviseSoftKeyboardEventSink
- Framework dei servizi di testo del metodo UnadviseSoftKeyboardEventSink, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742786"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>Metodo ISoftKbd:: UnadviseSoftKeyboardEventSink

Il metodo **ISoftKbd:: UnadviseSoftKeyboardEventSink** rimuove un sink di evento della tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TID* \[ in\]
</dt> <dd>

Identificatore del client proprietario del sink di evento della tastiera soft. Questo valore è stato passato quando è stato installato il sink di evento utilizzando [ISoftKbd:: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                                   | Descrizione                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Il metodo è stato eseguito correttamente.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Il parametro *TID* non è valido.<br/>                    |
| <dl> <dt>**Connetti \_ E \_ NOCONNECTION**</dt> </dl> | Il sink di notifica identificato da *TID* non è stato trovato.<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





