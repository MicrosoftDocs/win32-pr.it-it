---
title: Proprietà IMsRdpCameraRedirConfigCollection ByInstanceId
description: Restituisce un oggetto IMsRdpCameraRedirConfig dalla raccolta che corrisponde all'ID istanza specificato.
ms.tgt_platform: multiple
keywords:
- Proprietà ByInstanceId Servizi Desktop remoto
- Proprietà ByInstanceId Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto proprietà , ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e621efa61c6e033a9066da30fc6a2a97c76ebec94e9bfe848743f8b031b08d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080071"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>Proprietà IMsRdpCameraRedirConfigCollection::ByInstanceId

Restituisce un [oggetto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde all'ID istanza specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valore proprietà

Oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) che corrisponde all'ID istanza specificato.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>