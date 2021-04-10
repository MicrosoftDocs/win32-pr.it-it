---
title: Proprietà AdvancedSettings di IMsTscAx
description: Recupera un puntatore all'interfaccia IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964212"
---
# <a name="imstscaxadvancedsettings-property"></a>Proprietà IMsTscAx:: AdvancedSettings

Recupera un puntatore all'interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore di interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

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
</dt> </dl>

 

 





