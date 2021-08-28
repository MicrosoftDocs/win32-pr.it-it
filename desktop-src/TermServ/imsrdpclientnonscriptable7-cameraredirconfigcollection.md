---
title: Proprietà IMsRdpClientNonScriptable7 CameraRedirConfigCollection
description: Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Proprietà CameraRedirConfigCollection Servizi Desktop remoto
- Proprietà CameraRedirConfigCollection Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto , proprietà CameraRedirConfigCollection
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
ms.openlocfilehash: ea90c06403c1ba44e129867f2d739990a37ee178ebe5d0b8f4afd684b17eb09e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033171"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>Proprietà IMsRdpClientNonScriptable7::CameraRedirConfigCollection

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
| IID                      | IMsRdpClientNonScriptable7 IID è definito come \_ 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>