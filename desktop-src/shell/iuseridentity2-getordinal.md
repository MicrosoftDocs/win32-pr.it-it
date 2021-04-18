---
description: GetOrdinal non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'Metodo IUserIdentity2:: GetOrdinal (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980047"
---
# <a name="iuseridentity2getordinal-method"></a>Metodo IUserIdentity2:: GetOrdinal

\[**GetOrdinal** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Ottiene il numero ordinale per l'identità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwOrdinal* \[ out\]
</dt> <dd>

Tipo: **DWORD \** _

Puntatore a un valore _ *DWORD** che riceve il numero ordinale per l'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il numero ordinale determina l'ordine delle identità nell'elenco di identità, ma potrebbe non essere mantenuto durante le operazioni sulle identità. Per ottenere un valore univoco per un'identità, chiamare [**GetCookie**](iuseridentity-getcookie.md).

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetCookie**](iuseridentity-getcookie.md)
</dt> </dl>

 

 




