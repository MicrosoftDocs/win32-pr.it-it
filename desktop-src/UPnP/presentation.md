---
title: Presentazione
description: Presentazione è il passaggio finale del processo UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855958"
---
# <a name="presentation"></a>Presentazione

Presentazione è il passaggio finale del processo UPnP. Se un dispositivo ha un URL per la presentazione, un punto di controllo può recuperare una pagina da questo URL e caricare la pagina in un browser. A seconda delle funzionalità della pagina di presentazione e del dispositivo, il punto di controllo può controllare il dispositivo e visualizzare lo stato del dispositivo.

Il percorso della risorsa, che viene passato a [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante la registrazione, è la posizione in cui si trovano tutti i file rilevanti per la presentazione del dispositivo. Gli sviluppatori di dispositivi possono fornire pagine separate per ogni dispositivo incorporato. L'URL di presentazione nel modello di descrizione del dispositivo può essere un URL assoluto o un URL relativo. Per gli URL relativi, che sono relativi al percorso della risorsa, il modello di descrizione del dispositivo deve contenere un nome file. **IUPnPRegistrar** converte questo oggetto in un URL con il percorso effettivo. Per gli URL assoluti, il percorso non viene modificato.

Per supportare gli script sul lato client all'interno di una pagina di presentazione, le informazioni aggiuntive vengono in genere aggiunte all'URL sotto forma di "stringa di query". Le informazioni aggiuntive aggiunte sono l'URL del documento di descrizione del dispositivo e il UDN del dispositivo o del dispositivo incorporato. L'URL della descrizione del dispositivo può essere usato per caricare un documento di descrizione nello script, quindi controllare il dispositivo tramite i servizi. UDN viene usato per selezionare un dispositivo incorporato dal dispositivo radice.

Il formato dell'URL di presentazione modificato è: l'URL di presentazione effettivo, un punto interrogativo ("?"), l'URL Descrizione dispositivo, un segno più ("+"), il dispositivo UDN. Il punto interrogativo indica l'inizio della stringa di query.

Se l'URL di presentazione nel modello di descrizione del dispositivo è un URL assoluto e contiene già un punto interrogativo ("?"), le informazioni aggiuntive non vengono aggiunte all'URL della presentazione.



| Descrizione                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Nel modello di descrizione del dispositivo | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Generato dall'host del dispositivo       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Uno script lato client potrebbe dover estrarre l'URL della descrizione del dispositivo dall'URL di presentazione per caricare l'oggetto [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . Questa operazione viene eseguita prendendo la stringa di query e terminando il segno più ("+").


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



Nel caso di una pagina di presentazione per un dispositivo incorporato, sono necessarie alcune operazioni aggiuntive. Dopo aver caricato il [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), lo script deve ottenere la raccolta di dispositivi incorporati, quindi selezionare il dispositivo che corrisponde a UDN nella stringa di query. Lo script seguente mostra come selezionare il dispositivo incorporato per la pagina di presentazione corrente. Si presuppone che LightDesc sia già caricato.


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




