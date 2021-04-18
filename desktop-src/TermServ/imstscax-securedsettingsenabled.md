---
title: Proprietà SecuredSettingsEnabled di IMsTscAx
description: Indica se l'interfaccia IMsTscSecuredSettings è disponibile. Ovvero se la pagina Web contenente il controllo si trova attualmente in una delle aree di sicurezza URL Internet Explorer consentite.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302460"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a>Proprietà IMsTscAx:: SecuredSettingsEnabled

Indica se l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile. Ovvero se la pagina Web contenente il controllo si trova attualmente in una delle aree di sicurezza URL Internet Explorer consentite.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valore proprietà

Il valore di questo parametro è **true** se l'interfaccia è disponibile e **false** in caso contrario.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per eseguire una query per verificare se l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile prima di recuperare la proprietà [**SecuredSettings**](imstscax-securedsettings.md) .

Per un elenco di aree di sicurezza con URL limitati, vedere la pagina [relativa a come fornire la sicurezza del client RDP](providing-for-rdp-client-security.md) .

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

 

 





