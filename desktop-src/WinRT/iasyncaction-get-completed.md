---
description: Ottiene il metodo chiamato al completamento dell'azione asincrona.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Metodo IAsyncAction:: get_Completed'
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
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129239"
---
# <a name="iasyncactionget_completed-method"></a>Metodo IAsyncAction:: Get \_ Completed

Ottiene il metodo chiamato al completamento dell'azione asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gestore* \[ di out\]
</dt> <dd>

Tipo: **[ **asyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

Metodo che gestisce la notifica di completamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
