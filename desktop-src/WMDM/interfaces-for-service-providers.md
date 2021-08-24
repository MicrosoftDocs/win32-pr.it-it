---
title: Interfacce per i provider di servizi
description: Interfacce per i provider di servizi
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Gestione dispositivi multimediali, interfacce del provider di servizi
- Gestione dispositivi, interfacce del provider di servizi
- provider di servizi, interfacce
- informazioni di riferimento sulla programmazione, interfacce del provider di servizi
- informazioni di riferimento Windows Gestione dispositivi multimediali, interfacce del provider di servizi
- interfacce del provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a7b178ec0f3ab70f0a133a2286a97e294d449264061681fec540ae9b434c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766707"
---
# <a name="interfaces-for-service-providers"></a>Interfacce per i provider di servizi

In questa sezione vengono descritte le interfacce implementate Windows provider di servizi di Gestione dispositivi multimediali. I provider di servizi eseguono la maggior parte delle operazioni effettive di comunicazione con un dispositivo, perché implementano la maggior parte dei metodi SDK di Windows Gestione dispositivi multimediali chiamati dall'applicazione.

I provider di servizi non devono implementare tutte le interfacce elencate in questa sezione. Ad esempio, un dispositivo multimediale che non dispone di archiviazione su scheda non implementa le interfacce usate per controllare o esporre il contenuto. Nella pagina di riferimento appropriata viene indicato se è necessario un metodo o un'interfaccia.



| Interfaccia o classe                                     | Descrizione                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Classe helper che consente a un provider di servizi o a un provider di contenuto protetto di autenticare un'applicazione e creare firme MAC per i parametri sicuri.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | Fornisce al client (in genere Windows Gestione dispositivi multimediali) un enumeratore del dispositivo per i dispositivi supportati da questo provider di servizi.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Estende **IMDServiceProvider** fornendo un metodo per la creazione del dispositivo usando il percorso del dispositivo.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Estende **IMDServiceProvider2** fornendo un metodo per impostare le preferenze di enumerazione del dispositivo.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Fornisce un'associazione basata su istanza a un dispositivo multimediale. Usando questa interfaccia, il client può enumerare gli enumeratori dei supporti di archiviazione per il dispositivo, ottenere informazioni sul dispositivo e inviare comandi opachi (pass-through) al dispositivo.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Estende **IMDSPDevice** fornendo metodi per ottenere formati video estesi, ottenere i nomi dei dispositivi Plug and Play (PnP), abilitare l'uso delle pagine delle proprietà e consentire di ottenere un puntatore a un supporto di archiviazione dal nome. Questa interfaccia è facoltativa per il provider di servizi, ma è consigliata. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Estende **IMDSPDevice2** offrendo la possibilità di eseguire query sulle proprietà e sulle funzionalità del dispositivo in relazione al formato di un oggetto.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Fornisce metodi per il controllo dei dispositivi.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | Consente Windows Gestione dispositivi multimediali di delegare il trasferimento del contenuto al provider di servizi. In questo caso, Windows Gestione dispositivi multimediali non esegue alcuna elaborazione del contenuto prima di inviarlo al provider di servizi. Il provider di servizi ottiene il controllo completo dell'origine.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Enumera i dispositivi multimediali supportati da questo provider di servizi.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Enumera i supporti di archiviazione in un dispositivo e il contenuto in un supporto di archiviazione.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Contiene metodi per le operazioni di trasferimento dei dati in un oggetto di archiviazione.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Estende **IMDSPObject** offrendo una trasmissione più efficiente dei dati abilitati per DRM.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Imposta o ottiene la lunghezza di riproduzione, la posizione di riproduzione, l'offset di riproduzione o la lunghezza totale degli oggetti riproducibili in un supporto di archiviazione.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Recupera l'URL da cui è possibile scaricare i componenti aggiornati.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Fornisce un'associazione basata su istanze a un supporto di archiviazione in un dispositivo. Questa interfaccia crea oggetti di archiviazione, li recupera e fornisce l'accesso **all'interfaccia IMDSPEnumStorage** per enumerare le sottocartelle annidate all'interno dell'archiviazione corrente.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Estende **IMDSPStorage** ottenendo e impostando attributi estesi e rendendo possibile ottenere un puntatore all'archiviazione dal nome.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Estende **IMDSPStorage2** supportando i metadati.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Estende **IMDSPStorage3 supportando** gli oggetti playlist.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Recupera informazioni globali su un supporto di archiviazione, ad esempio la quantità di spazio disponibile e il numero totale di file.                                                                                                                                                                                              |



 

Il diagramma seguente illustra come ottenere le varie interfacce implementate da un provider di servizi. In questo diagramma le interfacce derivate vengono visualizzate nello stesso tag per la compattazione, quindi IMDServiceProvider/2/3 rappresenta tre interfacce: **IMDServiceProvider,** **IMDServiceProvider2** e **IMDServiceProvider3.** I metodi visualizzati vengono estesi solo da una di queste interfacce. Le interfacce derivate vengono ottenute chiamando **QueryInterface** sull'interfaccia di base dell'oggetto creato.

![diagramma che illustra come Gestione dispositivi Windows Media prevede di acquisire interfacce da un provider di servizi.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**Windows Interfacce DRM-Implemented multimediali**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




