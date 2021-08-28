---
title: Interfacce per le applicazioni
description: Interfacce per le applicazioni
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Gestione dispositivi multimediali, interfacce dell'applicazione
- Gestione dispositivi, interfacce dell'applicazione
- applicazioni desktop, interfacce
- informazioni di riferimento sulla programmazione, interfacce dell'applicazione
- informazioni di riferimento Windows Gestione dispositivi multimediali, interfacce dell'applicazione
- plug-in, interfacce
- interfacce dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690b8419a7f04ef2b4eab1db65266027bdf5bcf3a102e59a95030a290e3747ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619957"
---
# <a name="interfaces-for-applications"></a>Interfacce per le applicazioni

Questa sezione descrive le interfacce usate o implementate dalle applicazioni che usano l Windows SDK di Gestione dispositivi multimediali per comunicare con i dispositivi. Il termine "applicazione" usato qui indica qualsiasi eseguibile, plug-in o oggetto COM presente in un computer desktop e che richiede comunicazioni di alto livello con un dispositivo portatile connesso. Può includere un'applicazione lettore multimediale, un plug-in Windows Media Player (se è necessario l'accesso diretto a un dispositivo portatile) o un oggetto COM di misurazione del numero di riproduzione.

Alcune di queste interfacce vengono implementate dall'applicazione, mentre altre vengono chiamate dall'applicazione. La documentazione per ogni interfaccia indica se è implementata o chiamata (e, se implementata, se è facoltativa o obbligatoria).

Le interfacce o le classi seguenti vengono usate dalle applicazioni.



| Interfaccia o classe                                           | Descrizione                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classe CSecureChannelClient](csecurechannelclient-class.md) | Classe helper che consente alle applicazioni di autenticarsi, crittografare e decrittografare i dati e creare macs.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | L'interfaccia Windows gestione dispositivi multimediali per le applicazioni.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Estende **IWMDeviceManager** fornendo metodi di enumerazione avanzati e altri metodi.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Estende **l'interfaccia IWMDeviceManager2** fornendo un metodo che imposta la preferenza di enumerazione del dispositivo.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Fornisce metodi per esaminare ed esplorare un singolo dispositivo portatile.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Estende **IWMDMDevice** rendendo possibile ottenere i formati video supportati da un dispositivo, trovare una memoria in base al nome e usare le pagine delle proprietà.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Estende **IWMDMDevice2** fornendo metodi per eseguire query su un dispositivo per le proprietà, inviare i codici di controllo I/O del dispositivo e anche fornire metodi aggiornati per cercare le risorse di archiviazione e recuperare le funzionalità di formato del dispositivo. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Fornisce metodi per il controllo dei dispositivi.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Migliora l'efficienza delle operazioni dei dispositivi tramite l'aggregazione di più operazioni in un'unica sessione                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Enumera i dispositivi portatili collegati a un computer.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Enumera le risorse di archiviazione in un dispositivo.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Imposta e recupera le proprietà dei metadati (ad esempio artista, album, genere e così via) di una archiviazione.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Ottiene e imposta informazioni che controllano il modo in cui i file riproducibili nel dispositivo vengono gestiti **dall'interfaccia IWMDMDeviceControl**                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Recupera l'URL da cui è possibile scaricare i componenti aggiornati, se un trasferimento non riesce con un errore di revoca.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Fornisce metodi per esaminare ed esplorare un archivio (file, cartella, playlist) in un dispositivo.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Estende **IWMDMStorage** rendendo possibile ottenere una memoria figlio in base al nome e ottenere e impostare attributi estesi.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Estende **IWMDMStorage2** esponendo i metadati.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Estende **IWMDMStorage3** fornendo metodi per il recupero di un subset di metadati disponibili per un archivio e per l'impostazione e il recupero di un elenco di riferimenti ad altre risorse di archiviazione.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Consente di inserire, eliminare o spostare file all'interno di un dispositivo o tra un dispositivo e il computer.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Estende **IWMDMStorageControl** rendendo possibile l'impostazione del nome del file di destinazione quando si inserisce contenuto in un archivio.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Estende **IWMDMStorageControl2** rendendo possibile il passaggio di un puntatore a interfaccia **IWMDMMetaData.**                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Fornisce metodi per il recupero di informazioni globali su un supporto di archiviazione,ad esempio una scheda ROM flash, in un dispositivo.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Consente a un'applicazione di eseguire la misurazione, la sincronizzazione delle licenze e l'aggiornamento dei componenti DRM di un dispositivo.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Estende **IWMDRMDeviceApp** fornendo una nuova versione del **metodo QueryDeviceStatus.**                                                                                                                         |



 

Interfacce di callback

Le interfacce facoltative seguenti vengono implementate da un'applicazione per tenere traccia dello stato di avanzamento di una richiesta asincrona, ad esempio una richiesta di lettura o scrittura.



| Interfaccia                                      | Descrizione                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Consente alle applicazioni e ai provider di servizi di ricevere notifiche quando i dispositivi o le risorse di archiviazione di memoria (ad esempio le schede RAM) sono connesse o disconnesse dal computer. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Estende **IWMDMOperation** fornendo metodi per ottenere e impostare attributi estesi.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Estende **IWMDMOperation** fornendo un nuovo metodo per trasferire i dati non crittografati per migliorare l'efficienza.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Consente a un'applicazione di controllare la modalità di lettura o scrittura dei dati nel computer durante un trasferimento di file.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Estende il **metodo IWMDMProgress::End** fornendo un indicatore di stato.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Estende **IWMDMProgress2** fornendo parametri di input aggiuntivi per specificare l'ID evento e le informazioni specifiche del contesto.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Consente a un'applicazione di tenere traccia dello stato di avanzamento delle operazioni, ad esempio la formattazione di file multimediali o trasferimenti di file.                                                                  |



 

Il diagramma seguente illustra come viene acquisita la maggior parte delle interfacce dell'applicazione importanti **dall'interfaccia IWMDeviceManager** radice. Un'applicazione ottiene questa interfaccia radice tramite la creazione condivisa dell'oggetto MediaDevMgr, la richiesta dell'interfaccia **IComponentAuthenticate,** l'autenticazione del componente e quindi la richiesta **di IWMDeviceManager** (questi passaggi sono descritti in Autenticazione dell'applicazione). [](authenticating-the-application.md) Dopo aver acquisito questa interfaccia radice, viene chiamato [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) per creare un oggetto che implementa [**IWMDMEnumDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice) Altre interfacce vengono ottenute chiamando metodi sulle interfacce nell'ordine indicato. Le interfacce derivate, [**ad esempio IWMDMDevice2,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) vengono ottenute chiamando **QueryInterface** sull'interfaccia di base.

Nel diagramma seguente le interfacce derivate sono contrassegnate da barre, quindi "IWMDMStorage/2/3" indica **IWMDMStorage**, **IWMDMStorage2** e **IWMDMStorage3**.

![diagramma che illustra come ottenere le principali interfacce dell'applicazione in Gestione dispositivi multimediali di Windows.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




