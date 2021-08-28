---
title: Metodo IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.
ms.tgt_platform: multiple
keywords:
- Metodo CanSyncRemoteClipboardToLocalSession Servizi Desktop remoto
- Metodo CanSyncRemoteClipboardToLocalSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto metodo CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 40a9fc5d6dcdc2e96d9ce916bce0567cccc90adf10fcacc5d797f61ed292c116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000841"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Metodo IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession

Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.

## <a name="syntax"></a>Sintassi

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parametri

**TRUE** se gli Appunti remoti possono essere sincronizzati con la sessione locale; in caso contrario, **FALSE.**

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IMsRdpClipboard IID è definito come \_ 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>