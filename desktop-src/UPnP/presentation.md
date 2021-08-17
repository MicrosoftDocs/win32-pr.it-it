---
title: Presentazione
description: La presentazione è il passaggio finale del processo UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92f8457a881dc0414713e996d230261330c10911f2aea285a2e365ad0d59320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137194"
---
# <a name="presentation"></a>Presentazione

La presentazione è il passaggio finale del processo UPnP. Se un dispositivo ha un URL per la presentazione, un punto di controllo può recuperare una pagina da questo URL e caricare la pagina in un browser. A seconda delle funzionalità della pagina di presentazione e del dispositivo, il punto di controllo può controllare il dispositivo e visualizzare lo stato del dispositivo.

Il percorso della risorsa, che viene passato a [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante la registrazione, è il percorso in cui si trovano tutti i file rilevanti per la presentazione del dispositivo. Gli sviluppatori di dispositivi possono fornire pagine separate per ogni dispositivo incorporato. L'URL di presentazione nel modello di descrizione del dispositivo può essere un URL assoluto o un URL relativo. Per gli URL relativi, relativi al percorso della risorsa, il modello di descrizione del dispositivo deve contenere un nome file. **IUPnPRegistrar** lo converte in un URL con la posizione effettiva. Per gli URL assoluti, il percorso non viene modificato.

Per supportare gli script lato client all'interno di una pagina di presentazione, le informazioni aggiuntive vengono in genere aggiunte all'URL sotto forma di "stringa di query". Le informazioni aggiuntive aggiunte sono l'URL del documento di descrizione del dispositivo e la rete definita dall'utente del dispositivo o del dispositivo incorporato. L'URL di descrizione del dispositivo può essere usato per caricare un documento di descrizione nello script e quindi controllare il dispositivo tramite i relativi servizi. La rete definita dall'utente viene usata per selezionare un dispositivo incorporato dal dispositivo radice.

Il formato dell'URL di presentazione modificato è: l'URL di presentazione effettivo, un punto interrogativo ("?"), l'URL di descrizione del dispositivo, un segno più ("+"), il nome UDN del dispositivo. Il punto interrogativo indica l'inizio della stringa di query.

Se l'URL di presentazione nel modello di descrizione del dispositivo è un URL assoluto e contiene già un punto interrogativo ("?"), le informazioni aggiuntive non vengono aggiunte all'URL di presentazione.



| Descrizione                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Nel modello di descrizione del dispositivo | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Generato dall'host del dispositivo       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Potrebbe essere necessario estrarre l'URL di descrizione del dispositivo dall'URL di presentazione per caricare [**l'oggetto IUPnPDescriptionDocument.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) A tale scopo, prendere la stringa di query e terminarla in corrispondenza del segno più ("+").


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



Nel caso di una pagina di presentazione per un dispositivo incorporato, sono necessarie alcune operazioni aggiuntive. Dopo il caricamento di [**UPnPDescriptionDocument,**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)lo script deve ottenere la raccolta di dispositivi incorporati, quindi selezionare il dispositivo che corrisponde alla rete definita dall'utente nella stringa di query. Lo script seguente illustra come selezionare il dispositivo incorporato per la pagina di presentazione corrente. Si presuppone che LightDesc sia già caricato.


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



 

 




