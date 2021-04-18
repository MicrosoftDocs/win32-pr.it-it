---
description: Rappresenta un rapporto di Latitudine/Longitudine.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Oggetto LocationDisp. DispLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319027"
---
# <a name="locationdispdisplatlongreport-object"></a>Oggetto LocationDisp. DispLatLongReport

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Rappresenta un rapporto di Latitudine/Longitudine.

## <a name="members"></a>Membri

L'oggetto **LocationDisp. DispLatLongReport** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Le proprietà dell'oggetto **LocationDisp. DispLatLongReport** sono queste.



| Proprietà                                                                         | Tipo di accesso          | Descrizione                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Altitudine**](locationdisp-displatlongreport-altitude.md)<br/>           | Sola lettura<br/> | Altitudine corrente, in metri.<br/>                                                                                                                                                           |
| [**AltitudeError**](locationdisp-displatlongreport-altitudeerror.md)<br/> | Sola lettura<br/> | Errore di altitudine, in metri.<br/>                                                                                                                                                             |
| [**ErrorRadius**](locationdisp-displatlongreport-errorradius.md)<br/>     | Sola lettura<br/> | Distanza tra la posizione indicata, in metri. In combinazione con la posizione segnalata come origine, questo raggio descrive il cerchio in cui si trova il percorso effettivo proably.<br/> |
| [**Latitudine**](locationdisp-displatlongreport-latitude.md)<br/>           | Sola lettura<br/> | Latitudine corrente, in gradi.<br/>                                                                                                                                                          |
| [**Longitudine**](locationdisp-displatlongreport-longitude.md)<br/>         | Sola lettura<br/> | Longitudine corrente, in gradi.<br/>                                                                                                                                                         |
| [**Timestamp**](locationdisp-displatlongreport-timestamp.md)<br/>         | Sola lettura<br/> | Data e ora in cui è stato generato il report.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

È possibile recuperare questo oggetto tramite la proprietà [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) dell'oggetto [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) . È possibile ricevere questo oggetto tramite l'evento [**NewLatLongReport**](newlatlongreport.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 

