---
title: Interfaccia IMsRdpCameraRedirConfig
description: Rappresenta le configurazioni per una fotocamera disponibile per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto , descritta
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
ms.openlocfilehash: aa030d462a16eacd521709c5be534f3d90e14f446da519490ee62f0260766084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574541"
---
# <a name="imsrdpcameraredirconfig-interface"></a>Interfaccia IMsRdpCameraRedirConfig

Rappresenta le configurazioni per una fotocamera disponibile per il reindirizzamento.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpCameraRedirConfig** eredita da **IUnknown.** **IMsRdpCameraRedirConfig** include anche questi tipi di membri:

- [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IMsRdpCameraRedirConfig.**

| Proprietà         | Tipo di accesso           | Descrizione            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Sola lettura | Specifica se il dispositivo fotocamera esiste attualmente, ovvero se la fotocamera è connessa.   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Sola lettura |    Ottiene il nome descrittivo della fotocamera.    |
| [**Instanceid**](imsrdpcameraredirconfig-instanceid.md)      | Sola lettura |  Ottiene l'ID istanza della fotocamera.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Sola lettura |    Ottiene l'ID istanza del dispositivo padre della fotocamera.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lettura/Scrittura |  Specifica se la fotocamera viene reindirizzata o meno.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Sola lettura |   Ottiene il collegamento simbolico **dell'KSCATEGORY_VIDEO_CAMERA** per la fotocamera.   |

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