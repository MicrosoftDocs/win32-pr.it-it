---
title: Interfacce client DRM di Microsoft Windows Media
description: Interfacce client DRM di Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows MEDIA Format SDK, interfacce
- digital rights management (DRM), interfacce
- DRM (digital rights management),interfacce
- API estese del client DRM, interfacce
- API estese client,interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972224decdad339876e4f72c40cad5b3ba28de98446ff358fd36cb7f86bee0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931101"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Interfacce client DRM di Microsoft Windows Media

Nella tabella seguente vengono descritte le interfacce supportate dalle API client Windows Media DRM.



| Interfaccia                                                                    | Descrizione                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Fornisce la definizione per un callback di stato che è possibile implementare per gestire le operazioni DRM asincrone.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Fornisce un metodo per decrittografare il contenuto.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Fornisce un metodo per crittografare i dati sul posto.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Crittografa i dati da blocchi non contigui.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Estensione **dell'interfaccia IMFMediaEventGenerator** che fornisce un metodo per annullare le operazioni asincrone. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Consente il recupero di informazioni di stato avanzate sullo stato di avanzamento dell'individualizzazione.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Rappresenta una o più licenze nell'archivio licenze locale.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Consente il recupero di informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Abilita le operazioni di gestione per l'archivio licenze locale.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Fornisce opzioni di gestione aggiuntive per l'archivio licenze locale.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Consente alle applicazioni di eseguire query sui diritti e sullo stato della licenza per un file protetto.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | Fornisce i metodi necessari per creare un'applicazione ricevitore Microsoft Windows Media DRM per dispositivi di rete.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | Fornisce i metodi necessari per creare un'applicazione microsoft Windows Media DRM per dispositivi di rete.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Fornisce metodi che consentono l'acquisizione delle licenze con l'intervento dell'utente.                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | Crea gli altri oggetti delle API estese del client DRM di Microsoft Windows Media.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gestisce vari processi correlati alla sicurezza per il computer client e il sottosistema DRM.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gestisce la revoca e il rinnovo dei componenti.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Abilita la crittografia e la decrittografia dei buffer.                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](drm-programming-reference.md)
</dt> </dl>

 

 




