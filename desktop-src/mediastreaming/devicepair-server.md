---
title: Proprietà del server DevicePair (Asptlb. h)
description: Ottiene il server per la coppia di dispositivi di base attiva.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API di streaming multimediale delle proprietà del server
- API di streaming multimediale delle proprietà del server, interfaccia DevicePair
- API di streaming multimediale dell'interfaccia DevicePair, proprietà del server
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
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323912"
---
# <a name="devicepairserver-property"></a>Proprietà DevicePair:: Server

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
| Intestazione<br/> | <dl> <dt>Asptlb. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

