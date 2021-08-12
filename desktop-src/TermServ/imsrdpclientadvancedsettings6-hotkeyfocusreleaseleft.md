---
title: Proprietà IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseLeft
description: Specifica il codice del tasto virtuale da aggiungere a CTRL+ALT per determinare la sostituzione del tasto di scelta rapida per CTRL+ALT+freccia SINISTRA.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Proprietà HotKeyFocusReleaseLeft Servizi Desktop remoto
- Proprietà HotKeyFocusReleaseLeft Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà HotKeyFocusReleaseLeft
- Proprietà HotKeyFocusReleaseLeft Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà HotKeyFocusReleaseLeft
- Proprietà HotKeyFocusReleaseLeft Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà HotKeyFocusReleaseLeft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a5df8cd9c85ecccaf2de32a0e82ac604429f7b9f1e4801e3bfb025de8116d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607906"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a>Proprietà IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft

Specifica il codice del tasto virtuale da aggiungere a CTRL+ALT per determinare la sostituzione del tasto di scelta rapida per CTRL+ALT+freccia SINISTRA.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
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

 

 





