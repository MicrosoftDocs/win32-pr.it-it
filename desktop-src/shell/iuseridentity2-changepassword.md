---
description: ChangePassword non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'Metodo IUserIdentity2:: ChangePassword (Msident. h)'
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
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977890"
---
# <a name="iuseridentity2changepassword-method"></a>Metodo IUserIdentity2:: ChangePassword

\[**ChangePassword** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

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

*szOldPass* \[ in\]
</dt> <dd>

Tipo: **WCHAR \** _

Stringa di caratteri wide che contiene la password attualmente associata all'identità.

</dd> <dt>

_szNewPass * \[ in\]
</dt> <dd>

Tipo: **WCHAR \** _

Stringa di caratteri wide che contiene la nuova password da associare all'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il valore di *szOldPass* deve corrispondere alla password corrente dell'identità per l'applicazione di *szNewPass* . Un valore non corretto di *szOldPass* comporterà un valore restituito di E avrà \_ esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




