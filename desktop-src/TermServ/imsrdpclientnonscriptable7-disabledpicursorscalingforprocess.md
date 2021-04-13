---
title: Metodo IMsRdpClientNonScriptable7 DisableDpiCursorScalingForProcess
description: Disabilita la scalabilità locale del cursore del mouse ricevuta dal server, assicurando che la forma del cursore venga sottoposta a rendering correttamente senza modifiche.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisableDpiCursorScalingForProcess
- Metodo DisableDpiCursorScalingForProcess Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, metodo DisableDpiCursorScalingForProcess
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.DisableDpiCursorScalingForProcess
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a0de989fb0b1c3c644c73f214d368f2cab2ba5d5
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341406"
---
# <a name="imsrdpclientnonscriptable7disabledpicursorscalingforprocess-method"></a>IMsRdpClientNonScriptable7::D Metodo isableDpiCursorScalingForProcess

Disabilita la scalabilità locale del cursore del mouse ricevuta dal server, assicurando che la forma del cursore venga sottoposta a rendering correttamente senza modifiche.

## <a name="syntax"></a>Sintassi

```C++
HRESULT DisableDpiCursorScalingForProcess();
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

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
