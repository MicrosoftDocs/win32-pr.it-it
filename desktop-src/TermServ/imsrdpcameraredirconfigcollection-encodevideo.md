---
title: Proprietà EncodeVideo di IMsRdpCameraRedirConfigCollection
description: Specifica se il flusso video è con codifica H.264.
ms.tgt_platform: multiple
keywords:
- Codificare la proprietà EnVideo Servizi Desktop remoto
- Codificare la proprietà Envideo Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto , proprietà EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 9eda6fd63953425001906595b0cd8b594496e0f83974ba9d359ed43a639a4164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475961"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a>Proprietà IMsRdpCameraRedirConfigCollection::EncodeVideo

Specifica se il flusso video è con codifica H.264.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a>Valore proprietà

Valore che indica se il flusso video è con codifica H.264.

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