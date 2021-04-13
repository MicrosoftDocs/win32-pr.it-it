---
title: Interfacce client DRM di Microsoft Windows Media
description: Interfacce client DRM di Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK, interfacce
- Digital Rights Management (DRM), interfacce
- DRM (Digital Rights Management), interfacce
- API estese del client DRM, interfacce
- API estese client, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400085"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Interfacce client DRM di Microsoft Windows Media

Nella tabella seguente vengono descritte le interfacce supportate dalle API client DRM di Windows Media.



| Interfaccia                                                                    | Descrizione                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Fornisce la definizione per un callback di stato che è possibile implementare per gestire le operazioni DRM asincrone.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Fornisce un metodo per la decrittografia del contenuto.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Fornisce un metodo per la crittografia dei dati sul posto.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Crittografa i dati da blocchi non contigui.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Estensione dell'interfaccia **IMFMediaEventGenerator** che fornisce un metodo per annullare le operazioni asincrone. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Consente il recupero delle informazioni sullo stato avanzate sullo stato di individualizzazione.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Rappresenta una o più licenze nell'archivio licenze locale.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Consente il recupero di informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Abilita le operazioni di gestione per l'archivio licenze locale.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Fornisce opzioni di gestione aggiuntive per l'archivio licenze locale.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Consente alle applicazioni di eseguire query sui diritti e sullo stato di licenza per un file protetto.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | Fornisce i metodi necessari per creare un'applicazione del ricevitore di dispositivi di rete DRM di Microsoft Windows Media.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | Fornisce i metodi necessari per creare un'applicazione trasmittente Microsoft Windows Media DRM per dispositivi di rete.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Fornisce metodi che consentono l'acquisizione di licenze con l'intervento dell'utente.                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | Crea gli altri oggetti delle API estese del client DRM di Microsoft Windows Media.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gestisce vari processi correlati alla sicurezza per il computer client e il sottosistema DRM.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gestisce la revoca e il rinnovo dei componenti.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Consente la crittografia e la decrittografia dei buffer.                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](drm-programming-reference.md)
</dt> </dl>

 

 




