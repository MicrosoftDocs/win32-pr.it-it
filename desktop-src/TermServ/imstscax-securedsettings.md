---
title: Proprietà SecuredSettings di IMsTscAx
description: Recupera un puntatore all'interfaccia IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119774"
---
# <a name="imstscaxsecuredsettings-property"></a>Proprietà IMsTscAx:: SecuredSettings

Recupera un puntatore all'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore di interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Se il controllo è ospitato in una pagina Web e l'area di sicurezza dell'URL di Internet Explorer corrente non consente il recupero dell'indirizzo di interfaccia, questo metodo restituisce **E ha \_ esito negativo**.

Per le restrizioni sulla disponibilità dell'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) , vedere [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





