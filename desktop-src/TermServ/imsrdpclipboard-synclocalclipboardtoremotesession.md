---
title: Metodo IMsRdpClipboard SyncLocalClipboardToRemoteSession
description: Sincronizza gli Appunti locali con la sessione remota.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SyncLocalClipboardToRemoteSession
- Metodo SyncLocalClipboardToRemoteSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo SyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 55e407b86a34cf08d356676181d3225b4a5a768c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303660"
---
# <a name="imsrdpclipboardsynclocalclipboardtoremotesession-method"></a>Metodo IMsRdpClipboard:: SyncLocalClipboardToRemoteSession

Sincronizza gli Appunti locali con la sessione remota.

## <a name="syntax"></a>Sintassi

```C++
HRESULT SyncLocalClipboardToRemoteSession();
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
| IID                      | IID \_ IMsRdpClipboard è definito come 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>
