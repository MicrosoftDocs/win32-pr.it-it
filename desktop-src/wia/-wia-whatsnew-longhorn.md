---
description: In Windows Image Acquisition (WIA) 2,0 sono incluse molte nuove API Windows Image Acquisition (WIA).
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Novità di Windows Image Acquisition (WIA) 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f9d225185b8f1ff2d6441a7ddf0e8fd919ac98
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320838"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Novità di Windows Image Acquisition (WIA) 2,0

In Windows Image Acquisition (WIA) 2,0 sono incluse molte nuove API Windows Image Acquisition (WIA). Esistono inoltre alcune incompatibilità in avanti e indietro tra Windows Image Acquisition (WIA) 1,0 e il servizio WIA 2,0 fornito con Windows Vista. Alcune interfacce, strutture, proprietà e valori di proprietà di WIA 1,0 non sono supportati da e le applicazioni che le utilizzano non verranno eseguite in, Windows Vista e versioni successive. Analogamente, le applicazioni che utilizzano le nuove interfacce, le strutture, le proprietà e i valori delle proprietà introdotti con WIA 2,0 (vedere di seguito) non vengono eseguiti nelle versioni del sistema operativo precedenti a Windows Vista.

## <a name="new-api-for-wia-20"></a>Nuova API per WIA 2,0

### <a name="constants-lists-updated-for-wia-20"></a>Costanti: elenchi aggiornati per WIA 2,0

-   [**Costanti comuni della proprietà dell'elemento WIA**](-wia-wiaitempropcommonitem.md)
-   [**Costanti della proprietà informazioni sul dispositivo**](-wia-wiadeviceinfoprop.md)
-   [**Costanti della proprietà del dispositivo dello scanner**](-wia-wiaitempropscannerdevice.md)
-   [**Costanti della proprietà elemento WIA dello scanner**](-wia-wiaitempropscanneritem.md)
-   [**GUID categoria elemento WIA 2,0**](-wia-wia2-itemcategoryguids.md)
-   [**Costanti della dimensione della pagina WIA 2,0**](-wia-wia2-pagesizeconstants.md)
-   [**Flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Nuove strutture in WIA 2,0



| Argomento                                               | Contenuto                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.<br/>                                                                                                                                                                                                       |
| [**\_intestazione non elaborata WIA \_**](-wia-wia-raw-header.md)     | La struttura dell' [**\_ \_ intestazione non elaborata WIA**](-wia-wia-raw-header.md) definisce un'immagine nel formato dati non elaborati di un dispositivo e consente alle applicazioni di utilizzare il formato non elaborato nei trasferimenti WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | [**WiaTransferParams**](-wia-wiatransferparams.md) viene trasmesso a un'applicazione durante un trasferimento dati dal sistema di runtime WIA al metodo [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Nuove interfacce in WIA 2,0



| Argomento                                                         | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Utilizzato dalle applicazioni per enumerare gli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) nella cartella corrente dell'albero degli elementi.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | L'interfaccia [**IScanProfile**](-wia-iscanprofile.md) rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | L'interfaccia [**IScanProfileMgr**](-wia-iscanprofilemgr.md) fornisce metodi per la creazione, l'apertura, l'eliminazione e la gestione dei profili di analisi. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | L'interfaccia [**IScanProfileUI**](-wia-iscanprofileui.md) consente alle applicazioni di visualizzare una finestra di dialogo in modo che gli utenti possano creare, modificare ed eliminare i profili di analisi.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | L'interfaccia [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) consente alle applicazioni di visualizzare le finestre di errore, durante i trasferimenti di dati, da cui l'utente può scegliere se continuare, annullare o interrompere il trasferimento.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | L'interfaccia [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) viene usata per creare e gestire i dispositivi di acquisizione di immagini e per eseguire la registrazione per ricevere eventi del dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | L'interfaccia [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md) fornisce i metodi per gestire gli errori che possono verificarsi quando un'applicazione richiede i dati dell'immagine, sia per l'anteprima che per i bit finali. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | L'interfaccia [**IWiaImageFilter**](-wia-iwiaimagefilter.md) è un'interfaccia di estensione implementata dagli sviluppatori di filtri per l'elaborazione di immagini e chiamata da WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | L'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) fornisce applicazioni con le stesse funzionalità dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la possibilità di eseguire query sui dispositivi per individuarne le funzionalità, per accedere alle interfacce di trasferimento dei dati e alle proprietà degli elementi e per controllare il dispositivo). Fornisce inoltre all'applicazione la possibilità di creare e utilizzare in modo dinamico filtri di elaborazione delle immagini che possono provenire come estensioni dei driver di dispositivo WIA 2,0 disponibili in Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | L'interfaccia [**IWiaPreview**](-wia-iwiapreview.md) memorizza le immagini non filtrate internamente e le passa attraverso i filtri di elaborazione delle immagini. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | L'interfaccia [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) rileva le aree secondarie di un flusso di immagini e crea elementi [**IWiaItem2**](-wia-iwiaitem2.md) separati per ognuno di essi. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | L'interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) fornisce il trasferimento dei dati basato sul flusso. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | L'interfaccia [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) riceve i callback durante il trasferimento dei dati. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | L'interfaccia IWiaUIExtension2 fornisce metodi che sostituiscono l'interfaccia utente predefinita fornita dal sistema con un'interfaccia utente personalizzata e che forniscono un'icona di dispositivo personalizzata. I fornitori di dispositivi possono implementare questa interfaccia per fornire interfacce utente personalizzate per i dispositivi.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Panoramica nuove e modificate per WIA 2,0



| Argomento                                                                          | Contenuto |
|--------------------------------------------------------------------------------|----------|
| [Costanti](-wia-constants.md)                                                |          |
| [Funzioni](-wia-functions.md)                                                |          |
| [Interfacce](-wia-interfaces.md)                                              |          |
| [Schema del profilo di analisi](-wia-scan-profile-schema.md)                            |          |
| [Strutture](-wia-structures.md)                                              |          |
| [Trasferimento dei dati di immagine in WIA 2,0](-wia-transferring-image-data-in-wia2.md) |          |
| [Identificatori del tipo di dispositivo WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Costanti della proprietà WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Lascia commenti

Posta elettronica **sdkfdbk@microsoft.com** per effettuare segnalazioni di errori e richieste di funzionalità direttamente a Microsoft.

 

 




