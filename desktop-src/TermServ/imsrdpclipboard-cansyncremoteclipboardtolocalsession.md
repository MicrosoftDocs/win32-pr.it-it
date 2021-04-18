---
title: Metodo IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CanSyncRemoteClipboardToLocalSession
- Metodo CanSyncRemoteClipboardToLocalSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo CanSyncRemoteClipboardToLocalSession
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
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303661"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Metodo IMsRdpClipboard:: CanSyncRemoteClipboardToLocalSession

Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.

## <a name="syntax"></a>Sintassi

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parametri

**True** se gli Appunti remoti possono essere sincronizzati con la sessione locale; in caso contrario, **false**.

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