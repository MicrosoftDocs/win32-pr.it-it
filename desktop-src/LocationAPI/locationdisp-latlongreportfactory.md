---
description: Gestisce i report di Latitudine/Longitudine.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Oggetto LocationDisp. LatLongReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885537"
---
# <a name="locationdisplatlongreportfactory-object"></a>Oggetto LocationDisp. LatLongReportFactory

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Gestisce i report di Latitudine/Longitudine.

## <a name="members"></a>Membri

L'oggetto **LocationDisp. LatLongReportFactory** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **LocationDisp. LatLongReportFactory** ha questi metodi.



| Metodo                                                                                       | Descrizione                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-latlongreportfactory-listenforreports.md)               | Richiede gli eventi del rapporto Latitudine/Longitudine.<br/>                                         |
| [**RequestPermissions**](locationdisp-latlongreportfactory-requestpermissions.md)           | Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.<br/> |
| [**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Annulla le richieste per gli eventi del report di Latitudine/Longitudine.<br/>                             |



 

### <a name="properties"></a>Proprietà

Le proprietà dell'oggetto **LocationDisp. LatLongReportFactory** sono queste.



| Proprietà                                                                                | Tipo di accesso           | Descrizione                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**DesiredAccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Lettura/Scrittura<br/> | Valore di accuratezza desiderata corrente.<br/>                                                   |
| [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Sola lettura<br/>  | [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)corrente.<br/> |
| [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Lettura/Scrittura<br/> | Intervallo di eventi del report di Latitudine/Longitudine corrente in millisecondi.<br/>                 |
| [**Stato**](locationdisp-latlongreportfactory-status.md)<br/>                   | Sola lettura<br/>  | Stato corrente del report.<br/>                                                            |



 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare questo oggetto nel codice HTML.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



Nell'esempio di codice seguente viene illustrato come creare questo oggetto in JScript utilizzando Windows script host.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



Nell'esempio di codice seguente viene illustrato come creare questo oggetto in VBScript utilizzando Windows script host.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

