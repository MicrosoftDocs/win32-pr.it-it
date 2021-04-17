---
title: Metodo ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: Il metodo ISoftKbd AdviseSoftKeyboardEventSink installa un sink di evento della tastiera soft per gestire le notifiche OnKeySelection dalla tastiera soft.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Framework servizi di testo Metodo AdviseSoftKeyboardEventSink
- Framework dei servizi di testo del metodo AdviseSoftKeyboardEventSink, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400819"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>Metodo ISoftKbd:: AdviseSoftKeyboardEventSink

Il metodo **ISoftKbd:: AdviseSoftKeyboardEventSink** installa un sink di evento della tastiera soft per gestire le notifiche OnKeySelection dalla tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwKeyboardId* \[ in\]
</dt> <dd>

Identificatore della tastiera soft.

</dd> <dt>

*riid* \[ in\]
</dt> <dd>

Identificatore di interfaccia per l'interfaccia sink.

</dd> <dt>

*punk* \[ in\]
</dt> <dd>

Puntatore a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) per l'interfaccia sink specificata da *riid*. Questo parametro non può essere impostato su **null**.

</dd> <dt>

*pdwCookie* \[ out\]
</dt> <dd>

Puntatore al buffer in cui questo metodo recupera il "cookie" della tastiera soft usato per la connessione al client. Il cookie deve essere univoco per ogni connessione.

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

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

