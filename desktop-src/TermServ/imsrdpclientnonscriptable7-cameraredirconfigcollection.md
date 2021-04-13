---
title: Proprietà CameraRedirConfigCollection di IMsRdpClientNonScriptable7
description: Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CameraRedirConfigCollection
- Servizi Desktop remoto proprietà CameraRedirConfigCollection, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, proprietà CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341396"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>Proprietà IMsRdpClientNonScriptable7:: CameraRedirConfigCollection

Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Valore proprietà

Oggetto [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) che rappresenta la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 è definito come 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>