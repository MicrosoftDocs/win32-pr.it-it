---
title: Proprietà DisplayConnectionBar di IMsRdpClientAdvancedSettings
description: Specifica se utilizzare la barra di connessione. Il valore predefinito è VARIANT \_ true, che Abilita la proprietà.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà DisplayConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301315"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a>IMsRdpClientAdvancedSettings::D Proprietà isplayConnectionBar

Specifica se utilizzare la barra di connessione. Il valore predefinito è **Variant \_ true**, che Abilita la proprietà. L'impostazione di questa proprietà su **Variant \_ false** in un ambiente di scripting sicuro restituisce **E \_ non riesce**.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **Variant \_ false** per disabilitare la funzionalità o la **variante \_ true** per abilitare la funzionalità. Il valore predefinito è **Variant \_ true**.

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
</dt> </dl>

 

 





