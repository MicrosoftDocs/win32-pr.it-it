---
description: ChangePassword non è supportata e potrebbe essere modificata o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: Metodo IUserIdentity2::ChangePassword (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092698"
---
# <a name="iuseridentity2changepassword-method"></a>Metodo IUserIdentity2::ChangePassword

\[**ChangePassword** non è supportata e potrebbe essere modificata o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Imposta una nuova password per l'identità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szOldPass* \[ Pollici\]
</dt> <dd>

Tipo: **WCHAR \***

Stringa di caratteri wide che contiene la password attualmente associata all'identità.

</dd> <dt>

*szNewPass* \[ Pollici\]
</dt> <dd>

Tipo: **WCHAR \***

Stringa di caratteri wide che contiene la nuova password da associare all'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il valore di *szOldPass* deve corrispondere alla password corrente dell'identità per *l'applicazione di szNewPass.* Un valore errato *di szOldPass* restituirà E \_ FAIL.

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



 

 




