---
description: Specifica il nome dell'utente per conto del quale è prevista la registrazione del certificato.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Metodo ISCrdEnr:: seusername'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319355"
---
# <a name="iscrdenrsetusername-method"></a>Metodo ISCrdEnr:: seusername

Il metodo **Seusername** specifica il nome dell'utente per conto del quale è prevista la registrazione del certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo valore deve essere spaventato per la \_ registrazione \_ del \_ nome UPN (definito come 1) o per \_ registrare \_ il \_ nome compatibile con Sam \_ (definito come 2).

Impostare questo valore su SCARd \_ Registra \_ \_ nome UPN, se il nome specificato in *bstrUserName* è il nome dell'entità universale dell'utente, ad esempio " someone@example.com ". Il nome UPN dell'utente deve corrispondere a un nome SAM (Security Access Manager) esistente.

Impostare questo valore su SCARed \_ Registra \_ il \_ nome compatibile con Sam \_ , se il nome specificato in *bstrUserName* è il nome Sam dell'utente nel formato "dominio \\ utente".

</dd> <dt>

*bstrUserName* \[ in\]
</dt> <dd>

Nome dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Chiamare questo metodo per specificare il nome utente da emettere per la [*Smart Card*](../secgloss/s-gly.md). Un'alternativa a **Seusername** è [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).

Dopo che è stato specificato un nome utente, è possibile recuperare il relativo valore chiamando [**GetUserName**](iscrdenr-getusername.md).

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

[**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> </dl>

 

 
