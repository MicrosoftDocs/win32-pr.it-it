---
description: Gestisce i report degli indirizzi civici.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Oggetto LocationDisp.CivicAddressReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: e6e0efcc63d0d14934abe1f6be1444bf5b7eeaed2bfa0b0cd46efefed3f1bba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993023"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>Oggetto LocationDisp.CivicAddressReportFactory

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Gestisce i report degli indirizzi civici.

## <a name="members"></a>Membri

**L'oggetto LocationDisp.CivicAddressReportFactory** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto LocationDisp.CivicAddressReportFactory** dispone di questi metodi.



| Metodo                                                                                            | Descrizione                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Richiede eventi di report di indirizzo civico.<br/>                                              |
| [**Autorizzazioni di richiesta**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.<br/> |
| [**StopListeningForReports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Annulla le richieste di eventi di report di indirizzo civico.<br/>                                       |



 

### <a name="properties"></a>Proprietà

**L'oggetto LocationDisp.CivicAddressReportFactory** ha queste proprietà.



| Proprietà                                                                                        | Tipo di accesso           | Descrizione                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Sola lettura<br/>  | [**LocationDisp.DispCivicAddressReport corrente.**](locationdisp-dispcivicaddressreport.md)<br/> |
| [**DesiredAccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Lettura/Scrittura<br/> | Impostazione di accuratezza desiderata corrente.<br/>                                                           |
| [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Lettura/Scrittura<br/> | Intervallo corrente degli eventi del report degli indirizzi civici in millisecondi.<br/>                                |
| [**Status**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Sola lettura<br/>  | Stato del report corrente.<br/>                                                                      |



 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare questo oggetto nel codice HTML.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



Nell'esempio di codice seguente viene illustrato come creare questo oggetto in JScript usando Windows Host script.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



Nell'esempio di codice seguente viene illustrato come creare questo oggetto in VBScript usando Windows Script Host.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LocationDisp.CivicAddressReport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

