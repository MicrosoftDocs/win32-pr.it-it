---
title: Proprietà AuthenticationLevel di IMsRdpClientAdvancedSettings4
description: Specifica il livello di autenticazione da utilizzare per la connessione.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AuthenticationLevel
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
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873697"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a>Proprietà IMsRdpClientAdvancedSettings4:: AuthenticationLevel

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

Valore della proprietà **AuthenticationLevel** .

<dt>

0
</dt> <dd>

Nessuna autenticazione del server.

</dd> <dt>

1
</dt> <dd>

L'autenticazione server è obbligatoria e deve essere completata correttamente affinché la connessione continui.

</dd> <dt>

2
</dt> <dd>

Tentativo di autenticazione del server. Se l'autenticazione non riesce, all'utente verrà richiesto di annullare la connessione o di procedere senza l'autenticazione del server.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





