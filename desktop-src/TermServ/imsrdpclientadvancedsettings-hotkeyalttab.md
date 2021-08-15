---
title: Proprietà HotKeyAltTab IMsRdpClientAdvancedSettings
description: Specifica il codice del tasto virtuale da aggiungere ad ALT per determinare la sostituzione del tasto di scelta rapida per ALT+TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Proprietà HotKeyAltTab Servizi Desktop remoto
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto interfaccia , IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto proprietà , HotKeyAltTab
- Proprietà HotKeyAltTab Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto proprietà , HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22b50679b98bb57f40108287a303de3097cfe0bb3dc2fd552a957dae6479b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009891"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a>Proprietà IMsRdpClientAdvancedSettings::HotKeyAltTab

Specifica il codice del tasto virtuale da aggiungere ad ALT per determinare la sostituzione del tasto di scelta rapida per ALT+TAB.

Questa proprietà è valida solo quando la [**proprietà KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) non è abilitata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo codice della chiave virtuale. **VK \_ PRIOR** è il valore predefinito, con ALT+P UP come sequenza risultante.

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

 

 





