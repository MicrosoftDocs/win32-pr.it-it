---
title: Interfacce per i provider di contenuti sicuri
description: Interfacce per i provider di contenuti sicuri
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida di riferimento alla programmazione, contenuto protetto da DRM
- informazioni di riferimento per Windows Media Gestione dispositivi, contenuto protetto da DRM
- Contenuto protetto da DRM
- Windows Media Gestione dispositivi, Secure Content Provider (SCP)
- Gestione dispositivi, Secure Content Provider (SCP)
- Guida di riferimento alla programmazione, Secure Content Provider (SCP)
- informazioni di riferimento su Windows Media Gestione dispositivi, Secure Content Provider (SCP)
- provider di contenuti protetti (SCP)
- SCP (provider di contenuti protetto)
- Windows Media Gestione dispositivi, interfacce SCP
- Interfacce di Gestione dispositivi, SCP
- Guida di riferimento alla programmazione, interfacce SCP
- informazioni di riferimento sulle interfacce SCP di Windows Media Gestione dispositivi
- Interfacce SCP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298333"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfacce per i provider di contenuti sicuri

Un provider di contenuti protetto (SCP) è un componente plug-in che consente a Windows Media Gestione dispositivi di trasferire e richiedere informazioni sui diritti da contenuto protetto da DRM. Microsoft fornisce un componente SCP in grado di gestire file WMA e WMV protetti da DRM. Se il dispositivo o l'applicazione userà contenuto protetto da DRM di altri formati, deve creare un componente SCP implementando tutte le interfacce. In caso contrario, non sarà necessario utilizzare tali interfacce.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | Interfaccia principale del provider di contenuti protetti.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Estende **ISCPSecureAuthenticate** fornendo un metodo per ottenere un oggetto Session.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Utilizzato per scambiare il contenuto protetto e i diritti associati al contenuto.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Estende **ISCPSecureExchange** fornendo una nuova versione del metodo **TransferContainerData** .                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Estende **ISCPSecureExchange2** fornendo prestazioni di scambio dei dati migliorate e un metodo di callback completo del trasferimento.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Sottoposta a query da Windows Media Gestione dispositivi per determinare la proprietà del contenuto protetto.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Estende **ISCPSecureQuery** tramite la funzionalità che determina se il provider di contenuti protetti è responsabile del contenuto e, in tal caso, fornisce un URL per l'aggiornamento dei componenti revocati e per determinare quali componenti sono stati revocati. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Estende **ISCPSecureQuery2** fornendo un set di nuovi metodi per recuperare i diritti e prendere decisioni su un canale non crittografato.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Fornisce una gestione efficiente dello stato comune per più operazioni.                                                                                                                                                                                  |



 

 

 




