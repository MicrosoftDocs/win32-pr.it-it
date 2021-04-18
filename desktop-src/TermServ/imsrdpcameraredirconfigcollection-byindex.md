---
title: Proprietà ByIndex di IMsRdpCameraRedirConfigCollection
description: Restituisce un oggetto IMsRdpCameraRedirConfig in base al relativo indice nella raccolta.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ByIndex
- Servizi Desktop remoto proprietà ByIndex, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303646"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>Proprietà IMsRdpCameraRedirConfigCollection:: ByIndex

Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) in base al relativo indice nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valore proprietà

Oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) che corrisponde all'indice specificato.

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