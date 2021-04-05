---
title: Interfacce per i provider di servizi
description: Interfacce per i provider di servizi
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Media Gestione dispositivi, interfacce del provider di servizi
- Gestione dispositivi, interfacce del provider di servizi
- provider di servizi, interfacce
- Guida di riferimento alla programmazione, interfacce del provider di servizi
- informazioni di riferimento per Windows Media Gestione dispositivi, interfacce del provider di servizi
- interfacce del provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019d31f05674f0d9e492f8a73748500bc1d9d514
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711407"
---
# <a name="interfaces-for-service-providers"></a>Interfacce per i provider di servizi

In questa sezione vengono descritte le interfacce implementate dai provider di servizi Windows Media Gestione dispositivi. I provider di servizi eseguono la maggior parte del lavoro effettivo di comunicazione con un dispositivo, perché implementano la maggior parte dei metodi Windows Media Gestione dispositivi SDK chiamati dall'applicazione.

I provider di servizi non devono implementare tutte le interfacce elencate in questa sezione. Ad esempio, un dispositivo multimediale che non dispone di archiviazione a bordo non implementa le interfacce utilizzate per controllare o esporre il contenuto. Indica se è richiesto un metodo o un'interfaccia nella pagina di riferimento appropriata.



| Interfaccia o classe                                     | Descrizione                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Classe helper che consente a un provider di servizi o a un provider di contenuti protetto di autenticare un'applicazione e creare firme MAC per i parametri sicuri.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | Fornisce il client (in genere Windows Media Gestione dispositivi) con un enumeratore di dispositivo per i dispositivi supportati da questo provider di servizi.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Estende **IMDServiceProvider** fornendo un metodo per la creazione del dispositivo tramite il percorso del dispositivo.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Estende **IMDServiceProvider2** fornendo un metodo per l'impostazione delle preferenze di enumerazione del dispositivo.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Fornisce un'associazione basata su istanze a un dispositivo multimediale. Usando questa interfaccia, il client può enumerare gli enumeratori dei supporti di archiviazione per il dispositivo, ottenere informazioni sul dispositivo e inviare comandi opachi (pass-through) al dispositivo.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Estende **IMDSPDevice** fornendo metodi per il recupero di formati video estesi, il recupero di nomi di dispositivi Plug and Play (PNP), l'abilitazione dell'utilizzo delle pagine delle proprietà e la possibilità di ottenere un puntatore a un supporto di archiviazione dal nome. Questa interfaccia è facoltativa per il provider di servizi, ma è consigliata. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Estende **IMDSPDevice2** offrendo la possibilità di eseguire query sulle proprietà e sulle funzionalità del dispositivo in relazione al formato di un oggetto.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Fornisce metodi per il controllo dei dispositivi.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | Consente a Windows Media Gestione dispositivi di delegare il trasferimento del contenuto al provider di servizi. In questo caso Windows Media Gestione dispositivi non esegue alcuna elaborazione del contenuto prima di inviarlo al provider di servizi. Il provider di servizi ottiene il controllo completo dell'origine.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Enumera i dispositivi multimediali supportati da questo provider di servizi.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Enumera i supporti di archiviazione in un dispositivo e il contenuto in un supporto di archiviazione.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Contiene i metodi per le operazioni di trasferimento dei dati in un oggetto di archiviazione.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Estende **IMDSPObject** fornendo una trasmissione più efficiente dei dati abilitati per DRM.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Imposta o ottiene la lunghezza del gioco, la posizione di riproduzione, l'offset di riproduzione o la lunghezza totale degli oggetti riproducibili in un supporto di archiviazione.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Recupera l'URL da cui è possibile scaricare i componenti aggiornati.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Fornisce un'associazione basata su istanze con un supporto di archiviazione in un dispositivo. Questa interfaccia crea oggetti di archiviazione, recupera informazioni su di essi e fornisce l'accesso all'interfaccia **IMDSPEnumStorage** per l'enumerazione delle sottocartelle annidate all'interno dell'archiviazione corrente.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Estende **IMDSPStorage** ottenendo e impostando gli attributi estesi e rendendo possibile l'ottenimento di un puntatore all'archiviazione dal nome.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Estende **IMDSPStorage2** supportando i metadati.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Estende **IMDSPStorage3** supportando oggetti playlist.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Recupera le informazioni globali su un supporto di archiviazione, ad esempio la quantità di spazio disponibile e il numero totale di file.                                                                                                                                                                                              |



 

Nel diagramma seguente viene illustrato come ottenere le varie interfacce implementate da un provider di servizi. In questo diagramma, le interfacce derivate vengono visualizzate nello stesso tag per la compattazione, quindi IMDServiceProvider/2/3 rappresenta tre interfacce: **IMDServiceProvider**, **IMDServiceProvider2** e **IMDServiceProvider3**. I metodi mostrati vengono estesi solo da una di queste interfacce. Le interfacce derivate vengono ottenute chiamando **QueryInterface** sull'interfaccia di base dell'oggetto creato.

![diagramma che illustra il modo in cui gestione dispositivi Windows Media prevede di acquisire le interfacce da un provider di servizi.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**Interfacce DRM-Implemented Windows Media**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




