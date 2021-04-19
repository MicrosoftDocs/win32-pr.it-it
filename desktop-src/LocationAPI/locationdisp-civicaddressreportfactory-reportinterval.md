---
description: Intervallo di eventi del rapporto di indirizzo civico corrente in millisecondi.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Proprietà LocationDisp. CivicAddressReportFactory. ReportInterval
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
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319038"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Proprietà LocationDisp. CivicAddressReportFactory. ReportInterval

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Intervallo di eventi del rapporto di indirizzo civico corrente in millisecondi.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un **ULONG** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo valore è una richiesta per il provider di posizione. Non è necessario che il provider di località fornisca report nell'intervallo richiesto. Leggere il valore di questa proprietà per individuare l'impostazione dell'intervallo di report true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

