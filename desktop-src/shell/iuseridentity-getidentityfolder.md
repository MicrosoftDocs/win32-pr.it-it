---
description: GetIdentityFolder non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: Metodo IUserIdentity::GetIdentityFolder (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 20357dde27214177a454eb585dcd51182228c247da5aeae5ef887089b73ed85d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720607"
---
# <a name="iuseridentitygetidentityfolder-method"></a>Metodo IUserIdentity::GetIdentityFolder

\[**GetIdentityFolder** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Ottiene la cartella di file associata a questa identità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Obbligatorio. Valore che specifica se la cartella associata a questa identità è in roaming. Deve essere uno dei valori seguenti.

<dt>



 (GIF \_ ROAMING \_ FOLDER)


</dt> <dd>

La cartella è in roaming.

</dd> <dt>



 (GIF \_ CARTELLA NON \_ \_ IN ROAMING)


</dt> <dd>

La cartella è locale.

</dd> </dl> </dd> <dt>

*pszPath* \[ Pollici\]
</dt> <dd>

Tipo: **WCHAR \***

Puntatore a una stringa di caratteri wide che riceve il percorso della cartella.

</dd> <dt>

*ulBuffSize* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Valore che specifica le dimensioni di *pszPath.*

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

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




