---
title: Metodo IMsRdpClientNonScriptable6 SendLocation2D
description: Invia un valore di latitudine e longitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.
ms.tgt_platform: multiple
keywords:
- Metodo SendLocation2D Servizi Desktop remoto
- Metodo SendLocation2D Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable6
- Interfaccia IMsRdpClientNonScriptable6 Servizi Desktop remoto metodo SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 2e2e252f86249531c61922cf02f308bfaf2b76c2518ff9b420f5ec3fd80d9d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990141"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>Metodo IMsRdpClientNonScriptable6::SendLocation2D

Invia un valore di latitudine e longitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.

## <a name="syntax"></a>Sintassi

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Parametri

*latitudine* \[ Pollici\]

Latitudine di una posizione geografica. L'intervallo valido di valori di latitudine è compreso tra -90,0 e 90,0 gradi.

*longitudine* \[ Pollici\]

Longitudine di una posizione geografica. L'intervallo valido di valori di latitudine è compreso tra -180,0 e 180,0 gradi.

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1709 (build 16299)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IMsRdpClientNonScriptable6 IID è definito come \_ 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
