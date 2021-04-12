---
title: Metodo IMsRdpClientNonScriptable6 SendLocation3D
description: Invia un valore di latitudine, Longitudine e altitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendLocation3D
- Metodo SendLocation3D Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable6
- Interfaccia IMsRdpClientNonScriptable6 Servizi Desktop remoto, metodo SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480524"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a>Metodo IMsRdpClientNonScriptable6:: SendLocation3D

Invia un valore di latitudine, Longitudine e altitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.

## <a name="syntax"></a>Sintassi

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a>Parametri

*Latitudine* \[ in\]

Latitudine di una posizione geografica. L'intervallo valido di valori di latitudine è compreso tra-90,0 e 90,0 gradi.

*Longitudine* \[ in\]

Longitudine di una posizione geografica. L'intervallo valido di valori di latitudine è compreso tra-180,0 e 180,0 gradi.

*altitudine* \[ in\]

L'altitudine di una posizione geografica in metri.

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1709 (build 16299)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 è definito come 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
