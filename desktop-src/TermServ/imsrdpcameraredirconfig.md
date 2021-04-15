---
title: Interfaccia IMsRdpCameraRedirConfig
description: Rappresenta le configurazioni per una fotocamera disponibile per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520306"
---
# <a name="imsrdpcameraredirconfig-interface"></a>Interfaccia IMsRdpCameraRedirConfig

Rappresenta le configurazioni per una fotocamera disponibile per il reindirizzamento.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpCameraRedirConfig** eredita da **IUnknown**. **IMsRdpCameraRedirConfig** dispone anche di questi tipi di membri:

- [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpCameraRedirConfig** ha queste proprietà.

| Proprietà         | Tipo di accesso           | Descrizione            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Sola lettura | Specifica se il dispositivo della fotocamera è attualmente esistente (ovvero la fotocamera è connessa).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Sola lettura |    Ottiene il nome descrittivo della fotocamera.    |
| [**InstanceId**](imsrdpcameraredirconfig-instanceid.md)      | Sola lettura |  Ottiene l'ID dell'istanza della fotocamera.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Sola lettura |    Ottiene l'ID dell'istanza del dispositivo padre della fotocamera.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lettura/Scrittura |  Specifica se la fotocamera viene reindirizzata o meno.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Sola lettura |   Ottiene il collegamento simbolico dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.   |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vedi anche

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)