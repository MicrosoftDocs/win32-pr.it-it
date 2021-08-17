---
title: Proprietà AuthenticationLevel IMsRdpClientAdvancedSettings4
description: Specifica il livello di autenticazione da utilizzare per la connessione.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Proprietà AuthenticationLevel Servizi Desktop remoto
- Proprietà AuthenticationLevel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà AuthenticationLevel
- Proprietà AuthenticationLevel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà AuthenticationLevel
- Proprietà AuthenticationLevel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà AuthenticationLevel
- Proprietà AuthenticationLevel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà AuthenticationLevel
- Proprietà AuthenticationLevel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà AuthenticationLevel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01bed28e22f22e1dd14da4941027d5a99550cee49a45f40bf887ab27d7b940d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352568"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a>Proprietà IMsRdpClientAdvancedSettings4::AuthenticationLevel

Specifica il livello di autenticazione da utilizzare per la connessione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a>Valore proprietà

Valore della proprietà **AuthenticationLevel.**

<dt>

0
</dt> <dd>

Nessuna autenticazione del server.

</dd> <dt>

1
</dt> <dd>

L'autenticazione server è necessaria e deve essere completata correttamente per poter continuare la connessione.

</dd> <dt>

2
</dt> <dd>

Tentare l'autenticazione del server. Se l'autenticazione non riesce, all'utente verrà chiesto di annullare la connessione o di continuare senza l'autenticazione del server.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                                     |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings4 è definito come FBA7F64E-7345-4405-AE50-FA4A763DC0DE<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





