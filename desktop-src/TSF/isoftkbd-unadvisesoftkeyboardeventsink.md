---
title: Metodo ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc.h)
description: Il metodo ISoftKbd UnadviseSoftKeyboardEventSink rimuove un sink di evento della tastiera soft.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Metodo UnadviseSoftKeyboardEventSink Framework servizi di testo
- Metodo UnadviseSoftKeyboardEventSink Framework servizi di testo , interfaccia ISoftKbd
- Interfaccia ISoftKbd Framework servizi di testo metodo , UnadviseSoftKeyboardEventSink
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
ms.openlocfilehash: 90552c09e47d8a51f413f0588b12c8da5d44e665a6a5a51a79dc31717c6d56c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877111"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>Metodo ISoftKbd::UnadviseSoftKeyboardEventSink

Il **metodo ISoftKbd::UnadviseSoftKeyboardEventSink** rimuove un sink di evento della tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tid* \[ Pollici\]
</dt> <dd>

Identificatore del client proprietario del sink di evento della tastiera soft. Questo valore è stato passato quando il sink di evento è stato installato [usando ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                                   | Descrizione                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Il metodo è stato eseguito correttamente.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Il *parametro tid* non è valido.<br/>                    |
| <dl> <dt>**CONNECT \_ E \_ NOCONNECTION**</dt> </dl> | Il sink di consulenza identificato *da tid* non è stato trovato.<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





