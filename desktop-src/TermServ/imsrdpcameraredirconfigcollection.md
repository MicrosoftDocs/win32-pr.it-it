---
title: Interfaccia IMsRdpCameraRedirConfigCollection
description: Rappresenta la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123282"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>Interfaccia IMsRdpCameraRedirConfigCollection

 Rappresenta la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpCameraRedirConfigCollection** eredita da **IUnknown**. **IMsRdpCameraRedirConfigCollection** dispone anche di questi tipi di membri:

- [Metodi](#methods)
- [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpCameraRedirConfigCollection** dispone di questi metodi.

| Metodo            | Descrizione              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Aggiunge un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) alla raccolta (la fotocamera corrispondente non deve essere connessa).                   |
| [**Ripeti analisi**](imsrdpcameraredirconfigcollection-rescan.md)       |  Enumera i dispositivi della fotocamera connessa.                   |

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpCameraRedirConfigCollection** ha queste proprietà.

| Proprietà         | Tipo di accesso           | Descrizione            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | Sola lettura |  Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) in base al relativo indice nella raccolta.   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Sola lettura |    Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde all'ID istanza specificato.    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Sola lettura |  Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.  |
| [**Conteggio**](imsrdpcameraredirconfigcollection-count.md)                       | Sola lettura |    Restituisce il numero di oggetti [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) nell'insieme.   |
| [**EncodeVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Lettura/Scrittura |  Specifica se il flusso video è codificato con H. 264.  |
| [**EncodingQuality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Lettura/Scrittura |    Specifica la qualità della codifica (velocità in bit).   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Lettura/Scrittura |   Specifica se una nuova fotocamera viene reindirizzata per impostazione predefinita.    |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A            |

## <a name="see-also"></a>Vedi anche

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
