---
title: Metodo AddConfig IMsRdpCameraRedirConfigCollection
description: Aggiunge un oggetto IMsRdpCameraRedirConfig alla raccolta (la fotocamera corrispondente non deve essere connessa).
ms.tgt_platform: multiple
keywords:
- Metodo AddConfig Servizi Desktop remoto
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
ms.openlocfilehash: 88d4f7952497ca0afd970a979441f98864b2855ed3f36f3e556dc4241ed52769
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033651"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>Metodo IMsRdpCameraRedirConfigCollection::AddConfig

Aggiunge un [oggetto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) alla raccolta (la fotocamera corrispondente non deve essere connessa).

## <a name="syntax"></a>Sintassi

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parametri

*collegamento simbolico* \[ Pollici\]

Collegamento simbolico per il nuovo [oggetto IMsRdpCameraRedirConfig.](imsrdpcameraredirconfig.md)

*fRedirected* \[ Pollici\]

Specifica se la nuova fotocamera viene reindirizzata per impostazione predefinita.

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

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