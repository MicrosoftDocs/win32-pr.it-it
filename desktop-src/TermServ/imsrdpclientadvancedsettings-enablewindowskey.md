---
title: Proprietà EnableWindowsKey di IMsRdpClientAdvancedSettings
description: Specifica se la Windows chiave può essere usata nella sessione remota.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- Proprietà EnableWindowsKey Servizi Desktop remoto
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà EnableWindowsKey
- Proprietà EnableWindowsKey Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà EnableWindowsKey
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c639ee9bb31a5ef0092ec6a2aef8c0235639896a6d6934d8dc9cbadc42f40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608601"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a>Proprietà IMsRdpClientAdvancedSettings::EnableWindowsKey

Specifica se la Windows chiave può essere usata nella sessione remota.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la funzionalità o su un valore diverso da zero per abilitarla.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



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
</dt> </dl>

 

 





