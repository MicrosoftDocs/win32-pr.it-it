---
title: Metodo IMsRdpCameraRedirConfigCollection AddConfig
description: Aggiunge un oggetto IMsRdpCameraRedirConfig alla raccolta (la fotocamera corrispondente non deve essere connessa).
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddConfig
- Metodo AddConfig Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, metodo AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520305"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>Metodo IMsRdpCameraRedirConfigCollection:: AddConfig

Aggiunge un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) alla raccolta (la fotocamera corrispondente non deve essere connessa).

## <a name="syntax"></a>Sintassi

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parametri

*symbolicLink* \[ in\]

Collegamento simbolico per il nuovo oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .

*fRedirected* \[ in\]

Specifica se la nuova fotocamera viene reindirizzata per impostazione predefinita.

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

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