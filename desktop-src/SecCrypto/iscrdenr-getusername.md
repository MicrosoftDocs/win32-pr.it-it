---
description: Recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: Metodo ISCrdEnr::getUserName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b61dd43980049355621c2ee4085634303c55e0f9dac79db839602d07c7d61f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409449"
---
# <a name="iscrdenrgetusername-method"></a>Metodo ISCrdEnr::getUserName

Il **metodo getUserName** recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.

Prima di chiamare questo metodo, è necessario specificare il nome utente in una chiamata a [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) o [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo valore deve essere zero (0), SCARD ENROLL UPN NAME o \_ \_ \_ SCARD \_ ENROLL SAM \_ \_ COMPATIBLE \_ NAME.

Se questo valore è SCARD ENROLL UPN NAME, getUserName restituisce il nome \_ \_ dell'entità universale \_ (UPN) dell'utente, ad esempio "  someone@example.com ".

Se questo valore è SCARD ENROLL SAM COMPATIBLE NAME, il metodo restituisce il nome \_ \_ SAM \_ \_ (Security Access Manager) dell'utente nel formato "DOMAIN \\ USER".

Se questo valore è zero, il metodo restituisce il nome UPN dell'utente, se esistente. Se l'utente non ha un nome UPN, il metodo restituisce il nome SAM dell'utente.

</dd> <dt>

*pbstrUserName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

### <a name="vb"></a>VB

Stringa che rappresenta il nome dell'utente.

## <a name="remarks"></a>Commenti

È possibile specificare il nome dell'utente a cui viene emesso [*il smart card*](../secgloss/s-gly.md) chiamando [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) o [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md). Dopo aver specificato un nome utente, è possibile recuperarne il valore **chiamando getUserName.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
