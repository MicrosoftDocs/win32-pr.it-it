---
title: Proprietà DevicePair Server (Asptlb.h)
description: Ottiene il server per la coppia di dispositivi di base attiva.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- PROPRIETÀ server API Streaming multimediale
- Proprietà server API Streaming multimediale, interfaccia DevicePair
- Interfaccia DevicePair API Streaming multimediale, proprietà Server
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100725"
---
# <a name="devicepairserver-property"></a>Proprietà DevicePair::Server

Ottiene il server per la coppia di dispositivi di base attiva.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valore proprietà

Riceve un oggetto [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) che rappresenta il dispositivo server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Asptlb.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

