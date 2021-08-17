---
description: Intervallo di eventi del report dell'indirizzo civico corrente in millisecondi.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Proprietà LocationDisp.CivicAddressReportFactory.ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387162"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Proprietà LocationDisp.CivicAddressReportFactory.ReportInterval

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Intervallo di eventi del report dell'indirizzo civico corrente in millisecondi.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un ULONG di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Questo valore è una richiesta per il provider di località. Il provider di località non è necessario per fornire report all'intervallo richiesto. Leggere il valore di questa proprietà per individuare l'impostazione true dell'intervallo del report.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

