---
title: Proprietà BySymbolicLink di IMsRdpCameraRedirConfigCollection
description: Restituisce un oggetto IMsRdpCameraRedirConfig dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BySymbolicLink
- Servizi Desktop remoto proprietà BySymbolicLink, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà BySymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303650"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>IMsRdpCameraRedirConfigCollection::. Proprietà BySymbolicLink

Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valore proprietà

Oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) che corrisponde al collegamento simbolico specificato.

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