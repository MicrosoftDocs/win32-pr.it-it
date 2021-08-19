---
title: Proprietà DisableRdpdr di IMsTscAdvancedSettings
description: Specifica se il reindirizzamento della stampante e degli Appunti è abilitato.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Proprietà DisableRdpdr Servizi Desktop remoto
- Proprietà DisableRdpdr Servizi Desktop remoto, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto , proprietà DisableRdpdr
- Disabilitare la proprietà DisableRdpdr Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà DisableRdpdr
- Proprietà DisableRdpdr Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà DisableRdpdr
- Proprietà DisableRdpdr Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà DisableRdpdr
- Proprietà DisableRdpdr Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà DisableRdpdr
- Proprietà DisableRdpdr Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà DisableRdpdr
- Proprietà DisableRdpdr Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà DisableRdpdr
- Disabilitare la proprietà DisableRdpdr Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà DisableRdpdr
- Proprietà DisableRdpdr Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà DisableRdpdr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ce750f5f5dd9043648681558666df27528b22cdc7481426eca15fb0a5873a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125500"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a>Proprietà IMsTscAdvancedSettings::D isableRdpdr

Specifica se il reindirizzamento della stampante e degli Appunti è abilitato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **TRUE per** disabilitare il reindirizzamento o **FALSE** per abilitare il reindirizzamento.

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
| IID<br/>                      | IMsTscAdvancedSettings IID è definito come \_ 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



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

 

 





