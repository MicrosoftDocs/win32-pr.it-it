---
title: Proprietà allowBackgroundInput di IMsTscAdvancedSettings
description: Specifica se la modalità di input in background è abilitata.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà allowBackgroundInput
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
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400918"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a>Proprietà IMsTscAdvancedSettings:: allowBackgroundInput

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

Impostare questo parametro su 0 per disabilitare la modalità di input in background o un valore diverso da zero per abilitare la modalità di input in background.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d<br/> |



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

 

 





