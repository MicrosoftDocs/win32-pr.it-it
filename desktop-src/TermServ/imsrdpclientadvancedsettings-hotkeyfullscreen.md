---
title: Proprietà HotKeyFullScreen di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per passare alla modalità schermo intero.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963845"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a>Proprietà IMsRdpClientAdvancedSettings:: HotKeyFullScreen

Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per passare alla modalità schermo intero.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo codice della chiave virtuale. **VK \_ Annulla** è il valore predefinito.

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

 

 





