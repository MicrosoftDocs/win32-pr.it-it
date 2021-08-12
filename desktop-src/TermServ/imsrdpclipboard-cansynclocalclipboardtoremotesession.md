---
title: Metodo IMsRdpClipboard CanSyncLocalClipboardToRemoteSession
description: Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.
ms.tgt_platform: multiple
keywords:
- Metodo CanSyncLocalClipboardToRemoteSession Servizi Desktop remoto
- Metodo CanSyncLocalClipboardToRemoteSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: dabc12064ff43a2bb64a562d1aa3050681f46c31dd2698154beb1dafe3cfd85e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606916"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>Metodo IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession

Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.

## <a name="syntax"></a>Sintassi

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parametri

**TRUE** se gli Appunti locali possono essere sincronizzati con la sessione remota. in caso contrario, **FALSE.**

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

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