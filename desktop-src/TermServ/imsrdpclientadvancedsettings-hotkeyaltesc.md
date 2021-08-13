---
title: Proprietà IMsRdpClientAdvancedSettings HotKeyAltEsc
description: Specifica il codice del tasto virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT+ESC.
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- Proprietà HotKeyAltEsc Servizi Desktop remoto
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà HotKeyAltEsc
- Proprietà HotKeyAltEsc Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà HotKeyAltEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8757a2c8ba35ad2ba3080f340126fd689704769682a72389806eb905ecbf9aae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475461"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a>Proprietà IMsRdpClientAdvancedSettings::HotKeyAltEsc

Specifica il codice del tasto virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT+ESC.

Questa proprietà è valida solo quando la [**proprietà KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) non è abilitata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo codice della chiave virtuale. **VK \_ INSERT** è il valore predefinito, con ALT+INSERT come sequenza risultante.

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

 

 





