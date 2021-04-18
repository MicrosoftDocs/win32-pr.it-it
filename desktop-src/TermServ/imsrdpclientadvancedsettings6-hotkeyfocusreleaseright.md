---
title: Proprietà HotKeyFocusReleaseRight di IMsRdpClientAdvancedSettings6
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia destra.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyFocusReleaseRight
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyFocusReleaseRight
- Servizi Desktop remoto proprietà HotKeyFocusReleaseRight, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyFocusReleaseRight
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
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302578"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a>Proprietà IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseRight

Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + freccia destra.

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

 

 





