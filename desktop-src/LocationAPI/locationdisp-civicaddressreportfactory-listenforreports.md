---
description: Richiede eventi di report di indirizzo civico.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Metodo LocationDisp.CivicAddressReportFactory.ListenForReports (Locationapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 218684dcdb1c79b3b1a37517a4369ad492031cae1badfb9f0b16bbb6933289d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979771"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>Metodo LocationDisp.CivicAddressReportFactory.ListenForReports

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Richiede eventi di report di indirizzo civico.

## <a name="syntax"></a>Sintassi


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Numero (**doppia parola**) che rappresenta il tempo richiesto tra gli eventi del report degli indirizzi civici, espresso in millisecondi. Vedere la sezione Osservazioni.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il provider di posizione non è necessario per fornire l'accuratezza richiesta. Leggere il valore della proprietà [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) per individuare l'impostazione dell'intervallo di report reale.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Locationapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento NewCivicAddressReport**](newcivicaddressreport.md)
</dt> </dl>

 

