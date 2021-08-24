---
description: 'Proprietà LocationDisp.CivicAddressReportFactory.DesiredAccuracy: valore di accuratezza desiderato corrente.'
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Proprietà LocationDisp.CivicAddressReportFactory.DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca2d4f4a7be4afa800cfe81b5df7396be579197e7f997019f4ece3a39598c975
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693131"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>Proprietà LocationDisp.CivicAddressReportFactory.DesiredAccuracy

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Valore di accuratezza desiderato corrente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un ULONG di **lettura/scrittura.**



| Valore                                                                        | Significato                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Valore predefinito. Il sensore deve usare l'accuratezza per cui può ottimizzare l'utilizzo dell'energia elettrica e altre considerazioni sui costi.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Il sensore deve fornire il report più accurato possibile. È incluso l'utilizzo di servizi a pagamento o il consumo maggiore della batteria o della larghezza di banda della connessione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo valore è una richiesta al provider di posizione. Il provider di località non è necessario per fornire l'accuratezza richiesta. Leggere il valore di questa proprietà per individuare l'impostazione di accuratezza vera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

