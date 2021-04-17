---
title: Metodo IMsRdpClipboard SyncRemoteClipboardToLocalSession
description: Sincronizza gli Appunti remoti nella sessione locale.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SyncRemoteClipboardToLocalSession
- Metodo SyncRemoteClipboardToLocalSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo SyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d397d7c1ca4407a5125877721be9aa022f8132a7
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520322"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>Metodo IMsRdpClipboard:: SyncRemoteClipboardToLocalSession

Sincronizza gli Appunti remoti nella sessione locale.

## <a name="syntax"></a>Sintassi

```C++
HRESULT SyncRemoteClipboardToLocalSession();
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