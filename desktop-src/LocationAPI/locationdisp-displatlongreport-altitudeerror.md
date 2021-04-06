---
description: Errore di altitudine, in metri.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Proprietà LocationDisp. DispLatLongReport. AltitudeError
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
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883017"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>Proprietà LocationDisp. DispLatLongReport. AltitudeError

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Errore di altitudine, in metri.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).

## <a name="remarks"></a>Commenti

Non è necessario che i sensori di posizione forniscano questa proprietà. È necessario gestire le eccezioni quando si tenta di accedere a questa proprietà.

## <a name="examples"></a>Esempio

Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

