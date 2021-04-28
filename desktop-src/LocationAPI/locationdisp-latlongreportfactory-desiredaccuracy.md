---
description: 'Proprietà LocationDisp.LatLongReportFactory.DesiredAccuracy : valore corrente di accuratezza desiderata.'
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Proprietà LocationDisp.LatLongReportFactory.DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: afc5ec235df6c9e07a665410cb09e00f24305304
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088969"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>Proprietà LocationDisp.LatLongReportFactory.DesiredAccuracy

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Valore corrente di accuratezza desiderata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un ULONG di **lettura/scrittura.**



| Valore                                                                        | Significato                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Valore predefinito. Il sensore deve usare l'accuratezza per cui può ottimizzare l'utilizzo dell'energia elettrica e altre considerazioni sui costi.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Il sensore deve fornire il report più accurato possibile. È incluso l'utilizzo di servizi a pagamento o il consumo maggiore della batteria o della larghezza di banda della connessione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo valore è una richiesta al provider di posizione. Il provider di posizione non è necessario per fornire report in base all'intervallo richiesto. Leggere il valore di questa proprietà per individuare l'impostazione dell'intervallo di report reale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

