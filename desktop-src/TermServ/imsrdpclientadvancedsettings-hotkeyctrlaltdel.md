---
title: Proprietà HotKeyCtrlAltDel di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + CANC, detto anche firma di sicurezza sicura (SAS).
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400315"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a>Proprietà IMsRdpClientAdvancedSettings:: HotKeyCtrlAltDel

Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + CANC, detto anche firma di sicurezza sicura (SAS).

> [!Note]  
> CTRL + ALT + CANC non viene mai reindirizzato al server remoto, anche quando la proprietà [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) è abilitata; CTRL + ALT + CANC è la sequenza di firma di accesso condiviso locale.

 

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo codice della chiave virtuale. **VK \_ END** è il valore predefinito.

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

 

 





