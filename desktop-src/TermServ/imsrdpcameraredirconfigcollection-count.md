---
title: IMsRdpCameraRedirConfigCollection-proprietà conteggio
description: Restituisce il numero di oggetti IMsRdpCameraRedirConfig nell'insieme.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà Count
- Servizi Desktop remoto di proprietà Count, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà Count
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31927428b709136de87f436ad92cc6a78fa9795a
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480548"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>Proprietà IMsRdpCameraRedirConfigCollection:: count

Restituisce il numero di oggetti [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) nell'insieme.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Valore proprietà

Numero di oggetti [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) nell'insieme.

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