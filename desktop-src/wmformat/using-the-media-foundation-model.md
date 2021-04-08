---
title: Uso del modello di eventi Media Foundation
description: Uso del modello di eventi Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media Format SDK, DRM Media Foundation modello di eventi
- Windows Media Format SDK, Media Foundation modello di eventi
- Windows Media Format SDK, modello di eventi DRM
- Digital Rights Management (DRM) Media Foundation modello di eventi
- DRM (Digital Rights Management), modello di eventi Media Foundation
- Digital Rights Management (DRM), modello di eventi
- DRM (Digital Rights Management), modello di eventi
- Digital Rights Management (DRM), interfaccia IWMDRMEventGenerator
- DRM (Digital Rights Management), interfaccia IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046378"
---
# <a name="using-the-media-foundation-event-model"></a>Uso del modello di eventi Media Foundation

I metodi asincroni supportati dalle API estese del client Windows Media DRM usano lo stesso modello di eventi usato da Media Foundation SDK. Ogni oggetto che supporta i metodi asincroni implementa l'interfaccia [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , che può essere utilizzata per recuperare un evento quando viene completata un'operazione asincrona.

L'interfaccia **IWMDRMEventGenerator** eredita dall'interfaccia **IMFMediaEventGenerator** , documentata nella documentazione di Media Foundation SDK.

Il codice di esempio nell' [esempio di individualizzazione DRM](drm-individualization-example.md) usa il metodo **IMFMediaEventGenerator:: GetEvent** per recuperare gli eventi dalla coda uno alla volta. L'uso di **GetEvent** è più semplice rispetto all'uso di **IMFMediaEventGenerator:: BeginGetEvent** e **IMFMediaEventGenerator:: EndGetEvent** con un callback che rende gli esempi di codice più facili da comprendere. Se si usa **GetEvent** nel codice o si implementa **IMFAsyncCallback** e si usano **BeginGetEvent** e **EndGetEvent**, la logica per gestire l'evento dopo che è stata ricevuta è la stessa.

Molti dei metodi asincroni generano eventi che contengono riferimenti a oggetti che possono essere utilizzati per ottenere informazioni più dettagliate sullo stato. In questi casi, l'evento generato ha un puntatore **IUnknown** come valore, su cui è possibile eseguire query per recuperare l'interfaccia di stato. Nell'elenco seguente sono riepilogate le relazioni tra le chiamate asincrone, gli eventi generati e altre interfacce.

-   Il metodo [**IWMDRMLicenseManagement:: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) genera eventi **MEWMDRMLicenseBackupProgress** con le interfacce [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associate.
-   Il metodo [**IWMDRMLicenseManagement:: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) genera eventi **MEWMDRMLicenseRestoreProgress** con le interfacce [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associate.
-   Il metodo [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , quando viene usato per eseguire l'individualizzazione, genera eventi **MEWMDRMIndividualizationProgress** con le interfacce [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associate.
-   Il metodo [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , quando viene usato per preparare i dati per l'acquisizione di una licenza non invisibile all'utente, genera un evento **MEWMDRMLicenseAcquisitionCompleted** con un'interfaccia [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) associata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Per iniziare**](drm-getting-started.md)
</dt> <dt>

[Documentazione di Media Foundation SDK](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




