---
description: GetCookie non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: Metodo IUserIdentity::GetCookie (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e8b4abb13735b2ce370623ad8e5b79a8d9830b34a3d566fb57c0539d6f2c6095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220118"
---
# <a name="iuseridentitygetcookie-method"></a>Metodo IUserIdentity::GetCookie

\[**GetCookie** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Ottiene il cookie utilizzato per identificare in modo univoco questa identità utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*puidCookie* \[ Cambio\]
</dt> <dd>

Tipo: **\* GUID**

Puntatore a un **valore GUID** che riceve il cookie utilizzato per identificare in modo univoco questa identità utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**GetOrdinal**](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




