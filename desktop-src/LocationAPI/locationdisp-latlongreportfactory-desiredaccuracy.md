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
ms.openlocfilehash: 3deccb2dcc71a62b64a508e55759e5cc9c00b5cb0a7a59fb3390046371d2fac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129851"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>Proprietà LocationDisp.LatLongReportFactory.DesiredAccuracy

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

