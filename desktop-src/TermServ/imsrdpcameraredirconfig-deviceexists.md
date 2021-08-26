---
title: Proprietà DeviceExists IMsRdpCameraRedirConfig
description: Specifica se il dispositivo fotocamera esiste attualmente, ovvero se la fotocamera è connessa.
ms.tgt_platform: multiple
keywords:
- Proprietà DeviceExists Servizi Desktop remoto
- Proprietà DeviceExists Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto , proprietà DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 617c91491d88736ca60218d71f9dd5aa02ad0f9faeefdda6b872ba9262cec587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990661"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>Proprietà IMsRdpCameraRedirConfig::D eviceExists

Specifica se il dispositivo fotocamera esiste attualmente, ovvero se la fotocamera è connessa.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Valore proprietà

Valore che indica se il dispositivo fotocamera esiste attualmente, ovvero se la fotocamera è connessa.

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