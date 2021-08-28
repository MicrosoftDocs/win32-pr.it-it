---
title: Proprietà IMsRdpCameraRedirConfigCollection BySymbolicLink
description: Restituisce un oggetto IMsRdpCameraRedirConfig dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia KSCATEGORY_VIDEO_CAMERA **per** la fotocamera.
ms.tgt_platform: multiple
keywords:
- Proprietà BySymbolicLink Servizi Desktop remoto
- Proprietà BySymbolicLink Servizi Desktop remoto , interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto , proprietà BySymbolicLink
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
ms.openlocfilehash: a46cd3daf8cc4270473433bb0c4c20dee0616dba3619b056d33136e0d4dd8f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033631"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>IMsRdpCameraRedirConfigCollection::. BySymbolicLink - proprietà

Restituisce un [oggetto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia KSCATEGORY_VIDEO_CAMERA **per** la fotocamera.

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
| IID                      | IMsRdpCameraRedirConfigCollection IID è definito come \_ AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>