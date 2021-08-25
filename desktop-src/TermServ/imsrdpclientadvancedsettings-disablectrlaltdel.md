---
title: Proprietà IMsRdpClientAdvancedSettings DisableCtrlAltDel
description: Specifica se deve essere visualizzata la schermata esplicativa iniziale in Winlogon.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Proprietà DisableCtrlAltDel Servizi Desktop remoto
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto proprietà , DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà DisableCtrlAltDel
- Proprietà DisableCtrlAltDel Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà DisableCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c524945afe4fbaaa0498f579641a32d3f55f37e88335be82e8fa308fae502f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871056"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a>Proprietà IMsRdpClientAdvancedSettings::D isableCtrlAltDel

Specifica se deve essere visualizzata la schermata esplicativa iniziale in Winlogon.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
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

 

 





