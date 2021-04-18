---
title: Proprietà HotKeyCtrlEsc di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ESC.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
- Servizi Desktop remoto proprietà HotKeyCtrlEsc, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyCtrlEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301527"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a>Proprietà IMsRdpClientAdvancedSettings:: HotKeyCtrlEsc

Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ESC.

Questa proprietà è valida solo quando la proprietà [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) non è abilitata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo codice della chiave virtuale. **VK \_ HOME** è il valore predefinito, con Alt + Home come sequenza risultante.

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

 

 





