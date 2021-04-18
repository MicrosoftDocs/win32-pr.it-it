---
description: Valore di accuratezza desiderata corrente.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Proprietà LocationDisp. CivicAddressReportFactory. DesiredAccuracy
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
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319039"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>Proprietà LocationDisp. CivicAddressReportFactory. DesiredAccuracy

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Valore di accuratezza desiderata corrente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è un **ULONG** di lettura/scrittura.



| Valore                                                                        | Significato                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Valore predefinito. Il sensore deve usare l'accuratezza per cui può ottimizzare l'uso del risparmio energia e altre considerazioni sui costi.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Il sensore deve fornire il report più accurato possibile. È incluso l'utilizzo di servizi a pagamento o il consumo maggiore della batteria o della larghezza di banda della connessione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo valore è una richiesta al provider di posizione. Il provider di posizione non è necessario per fornire l'accuratezza richiesta. Leggere il valore di questa proprietà per individuare l'impostazione di accuratezza effettiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

