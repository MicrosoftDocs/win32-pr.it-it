---
title: Proprietà RedirectByDefault di IMsRdpCameraRedirConfigCollection
description: Specifica se una nuova fotocamera viene reindirizzata per impostazione predefinita.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectByDefault
- Servizi Desktop remoto proprietà RedirectByDefault, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123285"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a>Proprietà IMsRdpCameraRedirConfigCollection:: RedirectByDefault

Specifica se una nuova fotocamera viene reindirizzata per impostazione predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a>Valore proprietà

Valore che indica se una nuova fotocamera viene reindirizzata per impostazione predefinita.

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