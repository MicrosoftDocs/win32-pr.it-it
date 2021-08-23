---
description: Reimposta il conteggio interno delle interfacce recuperate nell'enumerazione .
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: Metodo IEnumUserIdentity::Reset (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: df70048760af47b380308eddab4ef5c044c8f6881374c83002944d6d76836ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969420"
---
# <a name="ienumuseridentityreset-method"></a>Metodo IEnumUserIdentity::Reset

\[**IEnumUserIdentity::Reset** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e](fastuserswitching.md)Desktop remoto .\]

Reimposta il conteggio interno delle interfacce recuperate nell'enumerazione .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica quale interfaccia deve essere recuperata. La chiamata a questo metodo reimposta il valore di questo conteggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> <dt>

[**IEnumUserIdentity::Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




