---
description: Gestisce i report degli indirizzi civici.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Oggetto LocationDisp. CivicAddressReportFactory
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
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758279"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>Oggetto LocationDisp. CivicAddressReportFactory

\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Gestisce i report degli indirizzi civici.

## <a name="members"></a>Membri

L'oggetto **LocationDisp. CivicAddressReportFactory** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **LocationDisp. CivicAddressReportFactory** ha questi metodi.



| Metodo                                                                                            | Descrizione                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Richiede eventi di report relativi all'indirizzo civico.<br/>                                              |
| [**RequestPermissions**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Apre una finestra di dialogo di sistema per richiedere l'autorizzazione utente per i dispositivi abilitati per la posizione.<br/> |
| [**StopListeningForReports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Annulla le richieste di eventi del report di indirizzo civico.<br/>                                       |



 

### <a name="properties"></a>Proprietà

Le proprietà dell'oggetto **LocationDisp. CivicAddressReportFactory** sono queste.



| Proprietà                                                                                        | Tipo di accesso           | Descrizione                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Sola lettura<br/>  | [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)corrente.<br/> |
| [**DesiredAccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Lettura/Scrittura<br/> | Impostazione di accuratezza desiderata corrente.<br/>                                                           |
| [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Lettura/Scrittura<br/> | Intervallo di eventi del rapporto di indirizzo civico corrente in millisecondi.<br/>                                |
| [**Stato**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Sola lettura<br/>  | Stato corrente del report.<br/>                                                                      |



 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare questo oggetto nel codice HTML.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



Nell'esempio di codice seguente viene illustrato come creare questo oggetto in JScript utilizzando Windows script host.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



Nell'esempio di codice seguente viene illustrato come creare questo oggetto in VBScript utilizzando Windows script host.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LocationDisp.CivicAddressReport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

