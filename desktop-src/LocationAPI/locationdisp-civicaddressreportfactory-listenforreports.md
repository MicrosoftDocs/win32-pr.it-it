---
description: Richiede eventi di report relativi all'indirizzo civico.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Metodo LocationDisp. CivicAddressReportFactory. ListenForReports (LocationApi. h)
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
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968591"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>LocationDisp. CivicAddressReportFactory. ListenForReports, metodo

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Richiede eventi di report relativi all'indirizzo civico.

## <a name="syntax"></a>Sintassi


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Numero (**doppia parola**) che rappresenta il tempo richiesto tra gli eventi del rapporto di indirizzo civico, in millisecondi. Vedere la sezione Osservazioni.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il provider di posizione non è necessario per fornire l'accuratezza richiesta. Leggere il valore della proprietà [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) per individuare l'impostazione dell'intervallo di report true.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>LocationApi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento NewCivicAddressReport**](newcivicaddressreport.md)
</dt> </dl>

 

