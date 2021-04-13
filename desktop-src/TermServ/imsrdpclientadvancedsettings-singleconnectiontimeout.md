---
title: Proprietà singleConnectionTimeout di IMsRdpClientAdvancedSettings
description: Specifica il periodo di tempo massimo, in secondi, durante il quale il controllo client attende una connessione a un indirizzo IP.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà singleConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400241"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a>Proprietà IMsRdpClientAdvancedSettings:: singleConnectionTimeout

Specifica il periodo di tempo massimo, in secondi, durante il quale il controllo client attende una connessione a un indirizzo IP.

Durante la connessione, il controllo può tentare di connettersi a più indirizzi IP.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a>Valore proprietà

Nuova ora, in secondi. Il valore massimo è 600.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**overallConnectionTimeout**](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





