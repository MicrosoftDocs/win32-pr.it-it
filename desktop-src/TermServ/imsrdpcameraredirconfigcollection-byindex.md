---
title: Proprietà IMsRdpCameraRedirConfigCollection ByIndex
description: Restituisce un oggetto IMsRdpCameraRedirConfig in base al relativo indice nella raccolta.
ms.tgt_platform: multiple
keywords:
- Proprietà ByIndex Servizi Desktop remoto
- Proprietà ByIndex Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto proprietà , ByIndex
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
ms.openlocfilehash: 375c0b110975c6ca791bbbe1f61a5b597b00316242484cd68ef018b7ef4ea88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138964"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>Proprietà IMsRdpCameraRedirConfigCollection::ByIndex

Restituisce un [oggetto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) in base al relativo indice nella raccolta.

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
| IID                      | IMsRdpCameraRedirConfigCollection IID è definito come \_ AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>