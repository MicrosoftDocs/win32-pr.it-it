---
title: Interfaccia IMsRdpClipboard
description: Rappresenta il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.
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
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123300"
---
# <a name="imsrdpclipboard-interface"></a>Interfaccia IMsRdpClipboard

Rappresenta il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti, ovvero se il valore della proprietà [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) è impostato su **true**.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClipboard** eredita da **IUnknown**. **IMsRdpClipboard** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpClipboard** dispone di questi metodi.


| Metodo        | Descrizione      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Sincronizza gli Appunti locali con la sessione remota.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Sincronizza gli Appunti remoti nella sessione locale.                      |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard è definito come 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable7:: Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
