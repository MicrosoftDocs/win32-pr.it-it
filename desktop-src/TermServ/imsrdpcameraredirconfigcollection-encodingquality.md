---
title: Proprietà EncodingQuality di IMsRdpCameraRedirConfigCollection
description: Specifica la qualità della codifica (velocità in bit).
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EncodingQuality
- Servizi Desktop remoto proprietà EncodingQuality, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480540"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>Proprietà IMsRdpCameraRedirConfigCollection:: EncodingQuality

Specifica la qualità della codifica (velocità in bit).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>Valore proprietà

Uno dei seguenti valori di enumerazione **CameraRedirEncodingQuality** che specifica la qualità della codifica (velocità in bit).

| Nome del membro enum | Valore |
|-----------------|--------|
| encodingQualityLow | 0x0000 |
| encodingQualityMedium | 0x0001 |
| encodingQualityHigh | 0x0002 |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>