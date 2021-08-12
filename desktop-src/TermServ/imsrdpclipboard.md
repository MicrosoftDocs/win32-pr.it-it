---
title: Interfaccia IMsRdpClipboard
description: Rappresenta il controller appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClipboard Servizi Desktop remoto
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a1ffc9a503365337676a11ccbdb872c1c7c7bed24eeb108fe1d565ced4de41d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606878"
---
# <a name="imsrdpclipboard-interface"></a>Interfaccia IMsRdpClipboard

Rappresenta il controller appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti, ovvero il valore della proprietà [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) è impostato su **True.**

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClipboard** eredita da **IUnknown**. **IMsRdpClipboard** include anche questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMsRdpClipboard** include questi metodi.


| Metodo        | Descrizione      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Sincronizza gli Appunti locali con la sessione remota.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Sincronizza gli Appunti remoti con la sessione locale.                      |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IMsRdpClipboard IID è definito come \_ 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable7::Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
