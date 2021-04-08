---
title: API di query del pacchetto
description: Informazioni sull'API di query del pacchetto, che è possibile usare per ottenere informazioni sui pacchetti dell'applicazione installati nel sistema. Ogni pacchetto dell'app contiene i file che costituiscono un'app di Windows e un file manifesto che descrive il software per Windows.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046569"
---
# <a name="package-query-api"></a>API di query del pacchetto

Informazioni sull'API di query del pacchetto, che è possibile usare per ottenere informazioni sui pacchetti dell'applicazione installati nel sistema. Ogni pacchetto dell'app contiene i file che costituiscono un'app di Windows e un file manifesto che descrive il software per Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosePackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Chiude un riferimento alle informazioni sul pacchetto specificate.<br/>                                                                                              |
| [**FindPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Trova i pacchetti con il nome di famiglia specificato per l'utente corrente. <br/>                                                                              |
| [**FormatApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Costruisce un [ID modello utente dell'applicazione](appx-packaging-glossary.md) dal nome della famiglia di pacchetti e dall'ID applicazione relativa del pacchetto (Praid). <br/> |
| [**GetApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Ottiene l' [ID del modello utente dell'applicazione](appx-packaging-glossary.md) per il processo specificato.<br/>                                                          |
| [**GetApplicationUserModelIdFromToken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Ottiene l' [ID del modello utente dell'applicazione](appx-packaging-glossary.md) per il token specificato.<br/>                                                            |
| [**GetCurrentApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Ottiene l' [ID del modello utente dell'applicazione](appx-packaging-glossary.md) per il processo corrente.<br/>                                                            |
| [**GetCurrentPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Ottiene il nome della famiglia di pacchetti per il processo chiamante.<br/>                                                                                                 |
| [**GetCurrentPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Ottiene il nome completo del pacchetto per il processo chiamante.<br/>                                                                                                   |
| [**GetCurrentPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Ottiene l'identificatore (ID) del pacchetto per il processo chiamante.<br/>                                                                                             |
| [**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Ottiene le informazioni sul pacchetto per il processo chiamante.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Ottiene le informazioni sul pacchetto per il processo chiamante, con l'opzione per specificare il tipo di cartella del pacchetto.<br/>                                                                                               |
| [**GetCurrentPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Ottiene il percorso del pacchetto per il processo chiamante.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Ottiene il percorso del pacchetto per il processo chiamante, con l'opzione per specificare il tipo di cartella del pacchetto.<br/>                                                                                                        |
| [**GetPackageApplicationIds**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Ottiene gli ID delle app nel pacchetto specificato.<br/>                                                                                                        |
| [**GetPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Ottiene il nome della famiglia di pacchetti per il processo specificato.<br/>                                                                                               |
| [**GetPackageFamilyNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Ottiene il nome della famiglia di pacchetti per il token specificato.<br/>                                                                                                 |
| [**GetPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Ottiene il nome completo del pacchetto per il processo specificato.<br/>                                                                                                 |
| [**GetPackageFullNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Ottiene il nome completo del pacchetto per il token specificato.<br/>                                                                                                   |
| [**GetPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Ottiene l'identificatore (ID) del pacchetto per il processo specificato.<br/>                                                                                           |
| [**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Ottiene le informazioni sul pacchetto per il pacchetto specificato.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Ottiene le informazioni sul pacchetto per il pacchetto specificato, con l'opzione per specificare il tipo di cartella del pacchetto.<br/>                                                                                               |
| [**Metodo GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Ottiene il percorso per il pacchetto specificato.<br/>                                                                                                              |
| [**GetPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Ottiene il percorso del pacchetto specificato.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Ottiene il percorso del pacchetto specificato, con l'opzione per specificare il tipo di cartella del pacchetto.<br/>                                                                                                               |
| [**GetPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Ottiene i pacchetti con il nome di famiglia specificato per l'utente corrente. <br/>                                                                               |
| [**GetStagedPackageOrigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Ottiene l'origine del pacchetto specificato.<br/>                                                                                                             |
| [**GetStagedPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Ottiene il percorso del pacchetto di gestione temporanea specificato.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Ottiene il percorso del pacchetto di gestione temporanea specificato, con l'opzione per specificare il tipo di cartella del pacchetto.<br/>                                                                                                        |
| [**OpenPackageInfoByFullName**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Apre le informazioni sul pacchetto del pacchetto specificato.<br/>                                                                                               |
| [**PackageFamilyNameFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Ottiene il nome della famiglia di pacchetti per il nome completo del pacchetto specificato.<br/>                                                                                     |
| [**PackageFamilyNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Ottiene il nome della famiglia di pacchetti per l'identificatore del pacchetto specificato.<br/>                                                                                    |
| [**PackageFullNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Ottiene il nome completo del pacchetto per l'identificatore (ID) del pacchetto specificato.<br/>                                                                                 |
| [**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Ottiene l'identificatore (ID) del pacchetto per il nome completo del pacchetto specificato.<br/>                                                                                 |
| [**PackageNameAndPublisherIdFromFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Ottiene il nome del pacchetto e l'identificatore del server di pubblicazione (ID) per il nome della famiglia di pacchetti specificato.<br/>                                                            |
| [**ParseApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Decostruisce un [ID modello utente dell'applicazione](appx-packaging-glossary.md) per il nome della famiglia di pacchetti e l'ID applicazione relativa del pacchetto (Praid).<br/>      |
| [**PackageOrigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Specifica l'origine di un pacchetto. <br/>                                                                                                                   |
| [**Costanti Identity**](identity-constants.md)<br/>                                           | Specifica la lunghezza delle stringhe per i campi Identity del pacchetto.<br/>                                                                                |
| [**Costanti pacchetto**](package-constants.md)<br/>                                             | Specifica la modalità di elaborazione dei pacchetti.<br/>                                                                                                           |
| [**\_ID pacchetto**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Rappresenta le informazioni di identificazione del pacchetto, ad esempio il nome, la versione e il server di pubblicazione.<br/>                                                                  |
| [**informazioni sul pacchetto \_**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Rappresenta le informazioni di identificazione del pacchetto che includono l'identificatore del pacchetto, il nome completo e il percorso di installazione.<br/>                                  |
| [**\_versione pacchetto**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Rappresenta le informazioni sulla versione del pacchetto.<br/>                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Concetti**
</dt> <dt>

[Distribuzione e pacchetti dell'applicazione](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[Glossario](appx-packaging-glossary.md)
</dt> <dt>

**Riferimento**
</dt> <dt>

[Schema del manifesto del pacchetto dell'applicazione](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[API per la creazione di pacchetti](interfaces.md)
</dt> <dt>

[API per la distribuzione di pacchetti](package-deployment-api.md)
</dt> </dl>

 

