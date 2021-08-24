---
description: Molte nuove API WIA (Windows Image Acquisition) sono incluse in Windows Image Acquisition (WIA) 2.0.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Novità dell'acquisizione Windows immagini (WIA) 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef5fdc2f70c7b0a7c25e3e9df68b82d05b7fd1a53eb7ec3613962f975e5c1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592951"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Novità dell'acquisizione Windows immagini (WIA) 2.0

Molte nuove API WIA (Windows Image Acquisition) sono incluse in Windows Image Acquisition (WIA) 2.0. Esistono inoltre alcune incompatibilità in avanti e indietro tra Windows Image Acquisition (WIA) 1.0 e il servizio WIA 2.0 fornito con Windows Vista. Alcune interfacce, strutture, proprietà e valori di proprietà di WIA 1.0 non sono supportati da e le applicazioni che le usano non verranno eseguite Windows Vista e versioni successive. Analogamente, le applicazioni che usano le nuove interfacce, strutture, proprietà e valori di proprietà introdotti con WIA 2.0 (vedere di seguito) non verranno eseguite nelle versioni del sistema operativo precedenti a Windows Vista.

## <a name="new-api-for-wia-20"></a>Nuova API per WIA 2.0

### <a name="constants-lists-updated-for-wia-20"></a>Costanti: elenchi aggiornati per WIA 2.0

-   [**Costanti comuni delle proprietà degli elementi WIA**](-wia-wiaitempropcommonitem.md)
-   [**Costanti delle proprietà relative alle informazioni sul dispositivo**](-wia-wiadeviceinfoprop.md)
-   [**Costanti delle proprietà del dispositivo scanner**](-wia-wiaitempropscannerdevice.md)
-   [**Costanti delle proprietà degli elementi WIA dello scanner**](-wia-wiaitempropscanneritem.md)
-   [**GUID categoria elemento WIA 2.0**](-wia-wia2-itemcategoryguids.md)
-   [**Costanti per dimensioni di pagina WIA 2.0**](-wia-wia2-pagesizeconstants.md)
-   [**Flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Nuove strutture in WIA 2.0



| Argomento                                               | Contenuto                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.<br/>                                                                                                                                                                                                       |
| [**INTESTAZIONE WIA \_ RAW \_**](-wia-wia-raw-header.md)     | La [**struttura WIA \_ RAW \_ HEADER**](-wia-wia-raw-header.md) definisce un'immagine nel formato dati RAW di un dispositivo e consente alle applicazioni di usare il formato RAW nei trasferimenti WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | [**WiaTransferParams**](-wia-wiatransferparams.md) viene trasmesso a un'applicazione durante un trasferimento dei dati dal sistema di run-time WIA al [**metodo IWiaTransferCallback::TransferCallback.**](-wia-iwiatransfercallback-transfercallback.md)<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Nuove interfacce in WIA 2.0



| Argomento                                                         | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Usato dalle applicazioni per [**enumerare gli oggetti IWiaItem2**](-wia-iwiaitem2.md) nella cartella corrente dell'albero degli elementi.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | [**L'interfaccia IScanProfile**](-wia-iscanprofile.md) rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | [**L'interfaccia IScanProfileMgr**](-wia-iscanprofilemgr.md) fornisce metodi per la creazione, l'apertura, l'eliminazione e la gestione dei profili di analisi. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | [**L'interfaccia IScanProfileUI**](-wia-iscanprofileui.md) consente alle applicazioni di visualizzare una finestra di dialogo in modo che gli utenti possano creare, modificare ed eliminare profili di analisi.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | [**L'interfaccia IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) consente alle applicazioni di visualizzare le finestre di errore (durante i trasferimenti di dati) da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | [**L'interfaccia IWiaDevMgr2**](-wia-iwiadevmgr2.md) viene usata per creare e gestire i dispositivi di acquisizione delle immagini e per registrarsi per ricevere gli eventi dei dispositivi.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | [**L'interfaccia IWiaErrorHandler**](-wia-iwiaerrorhandler.md) fornisce metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede dati di immagine, sia per i bit di anteprima che per i bit finali. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | [**L'interfaccia IWiaImageFilter**](-wia-iwiaimagefilter.md) è un'interfaccia di estensione implementata dagli sviluppatori di filtri di elaborazione delle immagini e chiamata da WIA 2.0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | [**L'interfaccia IWiaItem2**](-wia-iwiaitem2.md) fornisce alle applicazioni le stesse funzionalità dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la possibilità di eseguire query sui dispositivi per individuarne le funzionalità, accedere alle interfacce di trasferimento dei dati e alle proprietà degli elementi e controllare il dispositivo). Offre anche alle applicazioni la possibilità di creare e usare dinamicamente filtri di elaborazione delle immagini che possono essere forniti come estensioni dei driver di dispositivo WIA 2.0 forniti in Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | [**L'interfaccia IWiaPreview**](-wia-iwiapreview.md) memorizza nella cache le immagini non filtrate internamente e le passa attraverso i filtri di elaborazione delle immagini. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | [**L'interfaccia IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) rileva le sottoaree di un flusso di immagini e crea elementi [**IWiaItem2**](-wia-iwiaitem2.md) separati per ognuno. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | [**L'interfaccia IWiaTransfer**](-wia-iwiatransfer.md) fornisce il trasferimento dei dati basato sul flusso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | [**L'interfaccia IWiaTransferCallback**](-wia-iwiatransfercallback.md) riceve i callback durante un trasferimento dei dati. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | L'interfaccia IWiaUIExtension2 fornisce metodi che sostituiscono l'interfaccia utente predefinita fornita dal sistema con un'interfaccia utente personalizzata e che forniscono un'icona del dispositivo personalizzata. I fornitori di dispositivi possono implementare questa interfaccia per fornire interfacce utente personalizzate per i dispositivi.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Panoramiche nuove e modificate per WIA 2.0



| Argomento                                                                          | Contenuto |
|--------------------------------------------------------------------------------|----------|
| [Costanti](-wia-constants.md)                                                |          |
| [Funzioni](-wia-functions.md)                                                |          |
| [Interfacce](-wia-interfaces.md)                                              |          |
| [Schema del profilo di analisi](-wia-scan-profile-schema.md)                            |          |
| [Strutture](-wia-structures.md)                                              |          |
| [Trasferimento di dati immagine in WIA 2.0](-wia-transferring-image-data-in-wia2.md) |          |
| [Identificatori di tipo di dispositivo WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Costanti delle proprietà WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Commenti e suggerimenti

Messaggio di posta elettronica **sdkfdbk@microsoft.com** per inviare segnalazioni di errori e richieste di funzionalità direttamente a Microsoft.

 

 




