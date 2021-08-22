---
description: Altitudine corrente, in metri. L'altitudine è relativa ai puntini di sospensione di riferimento.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Proprietà LocationDisp.DispLatLongReport.Altitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ee6c2cd4257d7f7db97b89a5af4603f5c5129b7f07fe9bfbe6444bb9d347422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067941"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>Proprietà LocationDisp.DispLatLongReport.Altitude

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Altitudine corrente, in metri. L'altitudine è relativa ai puntini di sospensione di riferimento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un numero di sola **lettura** (virgola mobile a precisione doppia).

## <a name="remarks"></a>Commenti

I sensori di posizione non sono necessari per fornire questa proprietà. È necessario gestire le eccezioni quando si tenta di accedere a questa proprietà.

Il **metodo Altitude** recupera l'altitudine relativa ai puntini di sospensione di riferimento definiti dall'ultima revisione del sistema geodetico mondiale (WGS 84), anziché dall'altitudine rispetto al livello del mare.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

