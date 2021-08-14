---
description: Ottiene il metodo chiamato al completamento dell'azione asincrona.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: Metodo IAsyncAction::get_Completed
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 90e26947f0771490334ee731b25576759943c44cc47a9fda6681da9aa1f11fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323442"
---
# <a name="iasyncactionget_completed-method"></a>Metodo IAsyncAction::get \_ Completed

Ottiene il metodo chiamato al completamento dell'azione asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gestore* \[ Cambio\]
</dt> <dd>

Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

Metodo che gestisce la notifica di completamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
