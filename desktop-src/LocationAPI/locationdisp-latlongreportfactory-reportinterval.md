---
description: Intervallo di eventi del report di latitudine/longitudine corrente in millisecondi.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Proprietà LocationDisp.LatLongReportFactory.ReportInterval
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
ms.openlocfilehash: d12ceab473ae9375a9a1a96ff28d5389cccf324f4a447f17df7c628a514dcf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386691"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>Proprietà LocationDisp.LatLongReportFactory.ReportInterval

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Intervallo di eventi del report di latitudine/longitudine corrente in millisecondi.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un ULONG di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Questo valore è una richiesta al provider di località. Il provider di località non è necessario per fornire report all'intervallo richiesto. Leggere il valore di questa proprietà per individuare l'impostazione true dell'intervallo del report.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

