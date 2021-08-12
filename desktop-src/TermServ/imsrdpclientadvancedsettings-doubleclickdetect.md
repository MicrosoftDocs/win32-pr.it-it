---
title: Proprietà DoubleClickDetect IMsRdpClientAdvancedSettings
description: Specifica se il client identifica i doppio clic per il server.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- Proprietà DoubleClickDetect Servizi Desktop remoto
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto proprietà , DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto proprietà , DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà DoubleClickDetect
- Proprietà DoubleClickDetect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà DoubleClickDetect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2d7a292bf307ffeac538cafd31dc7fb3ceeb1a54b1e768239ee169b04e0fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608736"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a>Proprietà IMsRdpClientAdvancedSettings::D oubleClickDetect

Specifica se il client identifica i doppio clic per il server.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
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

 

 





