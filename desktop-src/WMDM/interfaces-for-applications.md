---
title: Interfacce per le applicazioni
description: Interfacce per le applicazioni
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Media Gestione dispositivi, interfacce dell'applicazione
- Gestione dispositivi, interfacce dell'applicazione
- applicazioni desktop, interfacce
- Guida di riferimento alla programmazione, interfacce dell'applicazione
- informazioni di riferimento su Windows Media Gestione dispositivi, interfacce dell'applicazione
- plug-in, interfacce
- interfacce dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49d66272c42679fd38d01b0114a834ee6f33e92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330380"
---
# <a name="interfaces-for-applications"></a>Interfacce per le applicazioni

In questa sezione vengono descritte le interfacce utilizzate o implementate dalle applicazioni che utilizzano Windows Media Gestione dispositivi SDK per comunicare con i dispositivi. Il termine "applicazione" usato qui indica qualsiasi eseguibile, plug-in o oggetto COM presente in un computer desktop e necessita di comunicazioni di alto livello con un dispositivo portatile connesso. Questo può includere un'applicazione per Media Player, un plug-in di Windows Media Player (se è necessario l'accesso diretto a un dispositivo portatile) o un oggetto COM di misurazione del numero di riproduzione.

Alcune di queste interfacce vengono implementate dall'applicazione, mentre altre vengono chiamate dall'applicazione. La documentazione per ogni interfaccia indica se è implementata o chiamata (e se implementata, se è facoltativa o obbligatoria).

Le interfacce o le classi seguenti vengono utilizzate dalle applicazioni.



| Interfaccia o classe                                           | Descrizione                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classe CSecureChannelClient](csecurechannelclient-class.md) | Classe helper che consente alle applicazioni di autenticarsi, crittografare e decrittografare i dati e creare i computer Mac.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | Interfaccia Windows Media Gestione dispositivi di primo livello per le applicazioni.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Estende **IWMDeviceManager** fornendo metodi di enumerazione avanzati e altri metodi.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Estende l'interfaccia **IWMDeviceManager2** fornendo un metodo che imposta la preferenza di enumerazione del dispositivo.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Fornisce metodi per esaminare ed esplorare un singolo dispositivo portatile.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Estende **IWMDMDevice** consentendo di ottenere i formati video supportati da un dispositivo, trovare uno spazio di archiviazione in base al nome e usare le pagine delle proprietà.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Estende **IWMDMDevice2** fornendo metodi per eseguire una query su un dispositivo per le proprietà, inviare codici di controllo di I/O dei dispositivi e fornire metodi aggiornati per cercare le archiviazioni e recuperare le funzionalità del formato del dispositivo. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Fornisce metodi per il controllo dei dispositivi.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Migliora l'efficienza delle operazioni del dispositivo aggregando più operazioni in un'unica sessione                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Enumera i dispositivi portatili collegati a un computer.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Enumera le archiviazioni in un dispositivo.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Imposta e recupera le proprietà dei metadati, ad esempio artista, album, genere e così via, di una risorsa di archiviazione.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Ottiene e imposta le informazioni che controllano il modo in cui i file riproducibili nel dispositivo vengono gestiti dall'interfaccia **IWMDMDeviceControl**                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Recupera l'URL da cui è possibile scaricare i componenti aggiornati, se un trasferimento ha esito negativo con un errore di revoca.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Fornisce metodi per esaminare ed esplorare un'archiviazione (file, cartella, playlist) in un dispositivo.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Estende **IWMDMStorage** consentendo di ottenere una risorsa di archiviazione figlio in base al nome e di ottenere e impostare gli attributi estesi.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Estende **IWMDMStorage2** esponendo i metadati.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Estende **IWMDMStorage3** fornendo metodi per il recupero di un subset di metadati disponibili per una risorsa di archiviazione e per l'impostazione e il recupero di un elenco di riferimenti ad altre archiviazioni.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Consente di inserire, eliminare o spostare i file all'interno di un dispositivo o tra un dispositivo e il computer.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Estende **IWMDMStorageControl** rendendo possibile l'impostazione del nome del file di destinazione quando si inserisce il contenuto in una risorsa di archiviazione.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Estende **IWMDMStorageControl2** consentendo di passare un puntatore all'interfaccia **IWMDMMetaData** .                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Fornisce metodi per il recupero di informazioni globali su un supporto di archiviazione, ad esempio una scheda Flash ROM, in un dispositivo.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Consente a un'applicazione di eseguire la misurazione, la sincronizzazione delle licenze e l'aggiornamento dei componenti DRM di un dispositivo.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Estende **IWMDRMDeviceApp** fornendo una nuova versione del metodo **QueryDeviceStatus** .                                                                                                                         |



 

Interfacce di callback

Le seguenti interfacce facoltative sono implementate da un'applicazione per tenere traccia dello stato di avanzamento di una richiesta asincrona, ad esempio una richiesta di lettura o scrittura.



| Interfaccia                                      | Descrizione                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Consente ai provider di servizi e alle applicazioni di ricevere notifiche quando i dispositivi o le archiviazioni di memoria, ad esempio le schede RAM, sono connessi o disconnessi dal computer. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Estende **IWMDMOperation** fornendo i metodi per ottenere e impostare gli attributi estesi.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Estende **IWMDMOperation** fornendo un nuovo metodo per il trasferimento dei dati non crittografati per una maggiore efficienza.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Consente a un'applicazione di controllare il modo in cui i dati vengono letti o scritti nel computer durante un trasferimento di file.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Estende il metodo **IWMDMProgress:: end** fornendo un indicatore di stato.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Estende **IWMDMProgress2** fornendo parametri di input aggiuntivi per specificare l'ID evento e le informazioni specifiche del contesto.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Consente a un'applicazione di tenere traccia dello stato di avanzamento delle operazioni, ad esempio la formattazione dei supporti o dei trasferimenti di file.                                                                  |



 

Il diagramma seguente illustra il modo in cui la maggior parte delle importanti interfacce dell'applicazione vengono acquisite dall'interfaccia **IWMDeviceManager** radice. Un'applicazione ottiene questa interfaccia radice creando un oggetto MediaDevMgr, richiedendo l'interfaccia **IComponentAuthenticate** , autenticando il componente e quindi richiedendo il **IWMDeviceManager** . questi passaggi sono descritti in [autenticazione dell'applicazione](authenticating-the-application.md). Una volta acquisita questa interfaccia radice, viene chiamato [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) per creare un oggetto che implementa [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). Altre interfacce vengono ottenute chiamando metodi sulle interfacce nell'ordine indicato. Le interfacce derivate, ad esempio [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) , vengono ottenute chiamando **QueryInterface** sull'interfaccia di base.

Nel diagramma seguente le interfacce derivate sono contrassegnate da barre, quindi "IWMDMStorage/2/3" indicherà **IWMDMStorage**, **IWMDMStorage2** e **IWMDMStorage3**.

![diagramma che illustra come ottenere le principali interfacce dell'applicazione in gestione dispositivi Windows Media.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




