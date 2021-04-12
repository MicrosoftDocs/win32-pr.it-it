---
title: Proprietà InstanceId IMsRdpCameraRedirConfig
description: Ottiene l'ID dell'istanza della fotocamera.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà InstanceId
- Servizi Desktop remoto proprietà InstanceId, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, proprietà InstanceId
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
ms.openlocfilehash: 42654e84f64b25a051a78963339ca95d4ebf760f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104225291"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>Proprietà IMsRdpCameraRedirConfig:: InstanceId

Ottiene l'ID dell'istanza della fotocamera.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Valore proprietà

ID dell'istanza della fotocamera.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>