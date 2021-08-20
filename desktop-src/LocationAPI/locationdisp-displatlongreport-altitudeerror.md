---
description: Errore di altitudine, in metri.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Proprietà LocationDisp.DispLatLongReport.AltitudeError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d84c09a143808302a623ab7b098a105ef74ee4ad7aecfe3a4a172b765fcbdfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809527"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>Proprietà LocationDisp.DispLatLongReport.AltitudeError

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Errore di altitudine, in metri.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un numero di sola **lettura** (virgola mobile a precisione doppia).

## <a name="remarks"></a>Commenti

I sensori di posizione non sono necessari per fornire questa proprietà. È necessario gestire le eccezioni quando si tenta di accedere a questa proprietà.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

