---
description: L'interfaccia IUpdate definisce le proprietà seguenti.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Proprietà di IUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df3f67f95936ea54dd09131e605da9e439caa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526694"
---
# <a name="iupdate-properties"></a>Proprietà di IUpdate

L'interfaccia [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) definisce le proprietà seguenti.



| Proprietà                                                                           | Descrizione                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Ottiene un valore booleano che indica se l'aggiornamento è contrassegnato per essere selezionato automaticamente da Windows Update.                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Ottiene un'interfaccia che contiene informazioni sull'elenco ordinato degli aggiornamenti in bundle per l'aggiornamento.                                                                           |
| [**CanRequireSource**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Ottiene un valore booleano che indica se il supporto di origine dell'aggiornamento è necessario per l'installazione o la disinstallazione.                                                          |
| [**Categorie**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Ottiene un'interfaccia che contiene una raccolta di categorie a cui appartiene l'aggiornamento.                                                                                             |
| [**Scadenza**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Ottiene la data in base alla quale deve essere installato l'aggiornamento.                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Ottiene un valore booleano che indica se il contenuto con compressione delta è disponibile su un server per l'aggiornamento.                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Ottiene un valore booleano che indica se preferire il contenuto con compressione delta durante il download e l'installazione o la disinstallazione dell'aggiornamento se è disponibile contenuto con compressione delta. |
| [**DeploymentAction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Ottiene l'azione per la quale viene distribuito l'aggiornamento.                                                                                                                                   |
| [**Descrizione**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Ottiene la descrizione localizzata dell'aggiornamento.                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Ottiene le informazioni sul file di download dell'aggiornamento.                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Ottiene la priorità di download consigliata dell'aggiornamento.                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Ottiene un valore booleano che indica se le condizioni di licenza software Microsoft associate all'aggiornamento sono accettate per il computer.                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Ottiene il testo localizzato completo delle condizioni di licenza software Microsoft associate all'aggiornamento.                                                                           |
| [**HandlerID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Ottiene il gestore di installazione dell'aggiornamento.                                                                                                                                             |
| [**Identità**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Ottiene un'interfaccia contenente l'identificatore univoco dell'aggiornamento.                                                                                                                |
| [**Immagine**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Ottiene un'interfaccia che contiene informazioni su un'immagine associata all'aggiornamento.                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Ottiene un'interfaccia che contiene le opzioni di installazione dell'aggiornamento.                                                                                                             |
| [**Versione beta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Ottiene un valore booleano che indica se l'aggiornamento è una versione beta.                                                                                                           |
| [**Scaricata**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Ottiene un valore booleano che indica se tutto il contenuto dell'aggiornamento viene memorizzato nella cache del computer.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Ottiene un valore booleano che indica se un aggiornamento è nascosto da un utente.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Ottiene un valore booleano che indica se l'aggiornamento è installato in un computer quando viene eseguita la ricerca.                                                                     |
| [**IsMandatory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Ottiene un valore booleano che indica se l'installazione dell'aggiornamento è obbligatoria.                                                                                            |
| [**Disinstallabile**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Ottiene un valore booleano che indica se un utente può disinstallare l'aggiornamento da un computer.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Ottiene una raccolta di ID degli articoli della Microsoft Knowledge base associati all'aggiornamento.                                                                                      |
| [**Linguaggi**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Ottiene un'interfaccia che contiene le lingue supportate dall'aggiornamento.                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Ottiene l'ultima data di pubblicazione dell'aggiornamento, nella data e ora UTC (Coordinated Universal Time), nel server che distribuisce l'aggiornamento.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Ottiene le dimensioni massime di download dell'aggiornamento.                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Ottiene le dimensioni minime di download dell'aggiornamento.                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Ottiene una raccolta di stringhe specifiche della lingua che specificano i collegamenti ipertestuali per ottenere ulteriori informazioni sull'aggiornamento.                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Ottiene la classificazione di gravità del centro risposte per la sicurezza di Microsoft dell'aggiornamento.                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Ottiene la velocità di CPU consigliata utilizzata per installare l'aggiornamento, in megahertz (MHz).                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Ottiene lo spazio libero consigliato che dovrebbe essere disponibile sul disco rigido prima di installare l'aggiornamento. Lo spazio disponibile è specificato in megabyte (MB).                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Ottiene le dimensioni della memoria fisica consigliate che devono essere disponibili nel computer prima di installare l'aggiornamento. Le dimensioni della memoria fisica sono specificate in megabyte (MB).         |
| [**ReleaseNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Ottiene le note sulla versione localizzate per l'aggiornamento.                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Ottiene una raccolta di valori stringa che contengono gli ID dei bollettini di sicurezza associati all'aggiornamento.                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Ottiene una raccolta di identificatori degli aggiornamenti. Questa raccolta di identificatori specifica gli aggiornamenti sostituiti dall'aggiornamento.                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Ottiene un collegamento ipertestuale alle informazioni di supporto specifiche della lingua per l'aggiornamento.                                                                                                       |
| [**Titolo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Ottiene il titolo localizzato dell'aggiornamento.                                                                                                                                             |
| [**Tipo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Ottiene il tipo dell'aggiornamento.                                                                                                                                                        |
| [**UninstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Ottiene un'interfaccia che contiene le opzioni di disinstallazione per l'aggiornamento.                                                                                                          |
| [**UninstallationNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Ottiene le note di disinstallazione per l'aggiornamento.                                                                                                                                       |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Ottiene un'interfaccia che contiene i passaggi di disinstallazione per l'aggiornamento.                                                                                                            |



 

 

 



