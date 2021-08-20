---
description: Completa una richiesta asincrona per annullare la registrazione di una coda di lavoro con un'attività del servizio Utilità di pianificazione classi multimediali (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Funzione RtwqEndUnregisterWorkQueueWithMMCSS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793401"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>Funzione RtwqEndUnregisterWorkQueueWithMMCSS

Completa una richiesta asincrona per annullare la registrazione di una coda di lavoro con un'attività del servizio Utilità di pianificazione classi multimediali (MMCSS).

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pResult* 
</dt> <dd>

Puntatore [**all'interfaccia IMFAsyncResult.**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) Passare lo stesso puntatore ricevuto dall'oggetto callback nel [**metodo IRtwqAsyncCallback::Invoke.**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>        |
| Libreria<br/>                  | <dl> <dt>Rtworkq.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
