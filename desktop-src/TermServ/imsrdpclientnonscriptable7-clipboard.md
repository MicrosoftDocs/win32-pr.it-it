---
title: Proprietà Degli Appunti IMsRdpClientNonScriptable7
description: Ottiene il controller appunti utilizzato per sincronizzare gli Appunti locali e remoti se la sincronizzazione manuale degli Appunti è abilitata.
ms.tgt_platform: multiple
keywords:
- Proprietà Clipboard Servizi Desktop remoto
- Proprietà Clipboard Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto , proprietà Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 236666cbef369c4f2353ff524ceb7544e62f50d4a7e4a7ac59f3882057a92f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009641"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>Proprietà IMsRdpClientNonScriptable7::Clipboard

Ottiene il controller appunti utilizzato per sincronizzare gli Appunti locali e remoti se la sincronizzazione manuale degli Appunti è abilitata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valore proprietà

Oggetto [IMsRdpClipboard](imsrdpclipboard.md) che rappresenta il controller appunti usato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti, ovvero il valore della proprietà [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) è impostato su **True.**

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IMsRdpClientNonScriptable7 IID è definito come \_ 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>