---
description: Altitudine corrente, in metri. L'altitudine è relativa all'ellissoide di riferimento.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. DispLatLongReport. Altitude (proprietà)
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
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882122"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>LocationDisp. DispLatLongReport. Altitude (proprietà)

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Altitudine corrente, in metri. L'altitudine è relativa all'ellissoide di riferimento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).

## <a name="remarks"></a>Commenti

Non è necessario che i sensori di posizione forniscano questa proprietà. È necessario gestire le eccezioni quando si tenta di accedere a questa proprietà.

Il metodo **Altitude** recupera l'altitudine rispetto all'ellissoide di riferimento definito dall'ultima revisione del sistema geodetico mondiale (WGS 84), anziché dall'altitudine rispetto al livello Sea.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

