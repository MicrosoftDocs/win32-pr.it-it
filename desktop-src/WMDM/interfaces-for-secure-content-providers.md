---
title: Interfacce per provider di contenuti sicuri
description: Interfacce per provider di contenuti sicuri
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Gestione dispositivi multimediali, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- informazioni di riferimento sulla programmazione, contenuto protetto da DRM
- informazioni di riferimento Windows Gestione dispositivi multimediali, contenuto protetto da DRM
- Contenuto protetto da DRM
- Windows Gestione dispositivi multimediali, provider di contenuti sicuri (SCP)
- Gestione dispositivi, provider di contenuti sicuri (SCP)
- informazioni di riferimento sulla programmazione, provider di contenuti sicuri (SCP)
- informazioni di riferimento Windows Gestione dispositivi multimediali, provider di contenuti protetti (SCP)
- provider di contenuti sicuri (SCP)
- SCP (provider di contenuti sicuro)
- Windows Gestione dispositivi multimediali, interfacce SCP
- Gestione dispositivi, interfacce SCP
- informazioni di riferimento sulla programmazione, interfacce SCP
- informazioni di riferimento Windows interfacce SCP e Gestione dispositivi multimediali
- interfacce SCP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80b74cfc50fb6dcf328379c5c46696dc2ee097e2ed5c2507a2a4f14676efd85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119247341"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfacce per provider di contenuti sicuri

Un provider di contenuti sicuri (SCP) è un componente plug-in che consente Windows Gestione dispositivi multimediali di trasferire e richiedere informazioni sui diritti dal contenuto protetto da DRM. Microsoft fornisce un componente SCP in grado di gestire file WMA e WMV protetti da DRM. Se il dispositivo o l'applicazione userà contenuto protetto da DRM di altri formati, deve creare un componente SCP implementando tutte queste interfacce. In caso contrario, non sarà necessario usare queste interfacce.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | Interfaccia principale del provider di contenuti sicuro.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Estende **ISCPSecureAuthenticate** fornendo un modo per ottenere un oggetto sessione.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Usato per scambiare contenuto protetto e diritti associati al contenuto.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Estende **ISCPSecureExchange** fornendo una nuova versione del **metodo TransferContainerData.**                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Estende **ISCPSecureExchange2** offrendo prestazioni di scambio dei dati migliorate e un metodo di callback completo per il trasferimento.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | È possibile eseguire query Windows Gestione dispositivi multimediali per determinare la proprietà del contenuto protetto.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Estende **ISCPSecureQuery** tramite funzionalità che determinano se il provider di contenuti protetti è responsabile del contenuto e, in tal caso, fornendo un URL per l'aggiornamento dei componenti revocati e per determinare quali componenti sono stati revocati. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Estende **ISCPSecureQuery2** fornendo un set di nuovi metodi per recuperare i diritti e prendere decisioni su un canale chiaro.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Fornisce una gestione efficiente dello stato comune per più operazioni.                                                                                                                                                                                  |



 

 

 




