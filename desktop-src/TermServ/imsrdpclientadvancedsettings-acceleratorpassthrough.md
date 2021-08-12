---
title: Proprietà IMsRdpClientAdvancedSettings AcceleratorPassthrough
description: Specifica se i tasti di scelta rapida devono essere passati al server.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- Proprietà AcceleratorPassthrough Servizi Desktop remoto
- Proprietà AcceleratorPassthrough Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà AcceleratorPassthrough
- Proprietà AcceleratorPassthrough Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà AcceleratorPassthrough
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c422147848c2b2625acc518074468febb7593d4a97bb8080c1db7d4b1ba7c081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609255"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a>Proprietà IMsRdpClientAdvancedSettings::AcceleratorPassthrough

Specifica se i tasti di scelta rapida devono essere passati al server.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la funzionalità o su un valore diverso da zero per abilitarla. Il valore predefinito è un valore diverso da zero.

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

 

 





