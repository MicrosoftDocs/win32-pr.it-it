---
description: Recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Metodo ISCrdEnr:: GetUserName'
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
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348506"
---
# <a name="iscrdenrgetusername-method"></a>Metodo ISCrdEnr:: GetUserName

Il metodo **GetUserName** Recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.

Prima di chiamare questo metodo, è necessario specificare il nome utente in una chiamata a [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md) o [**ISCrdEnr:: seusername**](iscrdenr-setusername.md).

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

*dwFlags* \[ in\]
</dt> <dd>

Questo valore deve essere pari a zero (0), il nome UPN per la registrazione è stato spaventato \_ \_ o il \_ \_ \_ \_ nome compatibile con Sam per la registrazione \_ .

Se questo valore è SCARed \_ Registra \_ \_ nome UPN, **GetUserName** restituisce il nome dell'entità universale (UPN) dell'utente, ad esempio " someone@example.com ".

Se questo valore viene spaventato \_ , registra \_ il \_ nome compatibile con Sam \_ , il metodo restituisce il nome di gestione Access Manager (Sam) dell'utente nel formato "dominio \\ utente".

Se questo valore è zero, il metodo restituisce il nome UPN dell'utente, se esistente. Se l'utente non dispone di un nome UPN, il metodo restituisce il nome SAM dell'utente.

</dd> <dt>

*pbstrUserName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome dell'utente.

## <a name="remarks"></a>Commenti

È possibile specificare il nome dell'utente a cui viene rilasciata la [*Smart Card*](../secgloss/s-gly.md) chiamando [**ISCrdEnr:: seusername**](iscrdenr-setusername.md) o [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md). Dopo che è stato specificato un nome utente, è possibile recuperare il relativo valore chiamando **GetUserName**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr:: seusername**](iscrdenr-setusername.md)
</dt> </dl>

 

 
