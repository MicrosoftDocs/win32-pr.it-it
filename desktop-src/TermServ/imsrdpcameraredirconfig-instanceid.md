---
title: Proprietà InstanceId IMsRdpCameraRedirConfig
description: Ottiene l'ID istanza della fotocamera.
ms.tgt_platform: multiple
keywords:
- Proprietà InstanceId Servizi Desktop remoto
- Proprietà InstanceId Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto , proprietà InstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 621c865f9727cf484430d00609dcfcfac2431a514cf2bade714fdd4d81b0408c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401001"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>Proprietà IMsRdpCameraRedirConfig::InstanceId

Ottiene l'ID istanza della fotocamera.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Valore proprietà

ID istanza della fotocamera.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IMsRdpCameraRedirConfig IID è definito come \_ 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>