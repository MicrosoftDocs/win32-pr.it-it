---
description: Intervallo di eventi del report di Latitudine/Longitudine corrente in millisecondi.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Proprietà LocationDisp. LatLongReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232076"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>Proprietà LocationDisp. LatLongReportFactory. ReportInterval

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Intervallo di eventi del report di Latitudine/Longitudine corrente in millisecondi.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un **ULONG** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo valore è una richiesta al provider di posizione. Non è necessario che il provider di località fornisca report nell'intervallo richiesto. Leggere il valore di questa proprietà per individuare l'impostazione dell'intervallo di report true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

