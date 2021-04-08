---
title: Proprietà HotKeyFocusReleaseLeft di IMsRdpClientAdvancedSettings6
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia sinistra.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyFocusReleaseLeft
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyFocusReleaseLeft
- Servizi Desktop remoto proprietà HotKeyFocusReleaseLeft, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyFocusReleaseLeft
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
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740007"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a>Proprietà IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseLeft

Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia sinistra.

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

Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





