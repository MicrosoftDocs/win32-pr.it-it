---
description: Richiede gli eventi del rapporto Latitudine/Longitudine.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Metodo LocationDisp. LatLongReportFactory. ListenForReports (LocationApi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757337"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a>LocationDisp. LatLongReportFactory. ListenForReports, metodo

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Richiede gli eventi del rapporto Latitudine/Longitudine.

## <a name="syntax"></a>Sintassi


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Numero (**doppia parola**) che rappresenta il tempo richiesto tra gli eventi del rapporto di Latitudine/Longitudine, in millisecondi. Vedere la sezione Osservazioni.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Non è necessario che il provider di località fornisca report nell'intervallo richiesto. Leggere il valore della proprietà [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) per individuare l'impostazione dell'intervallo di report true.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [ascolto degli eventi del report LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>LocationApi. h</dt> </dl> |



 

