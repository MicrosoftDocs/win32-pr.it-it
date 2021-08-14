---
title: Proprietà IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseRight
description: Specifica il codice del tasto virtuale da aggiungere a CTRL+ALT per determinare la sostituzione del tasto di scelta rapida per CTRL+ALT+freccia DESTRA.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Proprietà HotKeyFocusReleaseRight Servizi Desktop remoto
- Proprietà HotKeyFocusReleaseRight Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà HotKeyFocusReleaseRight
- Proprietà HotKeyFocusReleaseRight Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà HotKeyFocusReleaseRight
- Proprietà HotKeyFocusReleaseRight Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà HotKeyFocusReleaseRight
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c508dd3007db9da47d8680b67d210d5e541351cdab7078e1ee6447b078638c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352275"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a>Proprietà IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight

Specifica il codice del tasto virtuale da aggiungere a CTRL+ALT per determinare la sostituzione del tasto di scelta rapida per CTRL+ALT+freccia DESTRA.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo codice della chiave virtuale.

## <a name="remarks"></a>Commenti

Questa proprietà è supportata solo dai Connessione Desktop remoto 6.1 e 7.0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





