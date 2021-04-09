---
title: Proprietà degli Appunti IMsRdpClientNonScriptable7
description: Ottiene il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà degli Appunti
- Servizi Desktop remoto proprietà degli Appunti, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, proprietà degli Appunti
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
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "103965441"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>Proprietà IMsRdpClientNonScriptable7:: Clipboard

Ottiene il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valore proprietà

Un [IMsRdpClipboard](imsrdpclipboard.md) che rappresenta il controller degli Appunti usato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti, ovvero se il valore della proprietà [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) è impostato su **true**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 è definito come 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>