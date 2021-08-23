---
title: IMsTscAdvancedSettings - proprietà allowBackgroundInput
description: Specifica se la modalità di input in background è abilitata.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Proprietà allowBackgroundInput Servizi Desktop remoto
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà allowBackgroundInput
- Proprietà allowBackgroundInput Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà allowBackgroundInput
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b79df16c3bcd1120344bc6189ace324e434ad4cbd7a831757e455e26f6d10902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657431"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a>Proprietà IMsTscAdvancedSettings::allowBackgroundInput

Specifica se la modalità di input in background è abilitata. Quando l'input in background è abilitato, il client può accettare l'input quando il client non ha lo stato attivo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la modalità di input in background o su un valore diverso da zero per abilitare la modalità di input in background.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





