---
title: Creazione di pacchetti, distribuzione e query delle app di Windows
description: Creare pacchetti dell'applicazione per le app di Windows a livello di codice e installare, aggiornare, eseguire query e disinstallare i pacchetti dell'app.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bfd1792e0b7b18f0dee04bca6f352e055b20f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117582"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Creazione di pacchetti, distribuzione e query delle app di Windows

È possibile distribuire, gestire e servire app di Windows (incluse le app UWPs e desktop) tramite i pacchetti dell'app msix/appx in base al formato OPC. Ogni pacchetto dell'app contiene i file che costituiscono l'app e un file manifesto che descrive il software per Windows.

## <a name="introduction"></a>Introduzione

In genere, gli sviluppatori creano e firmano i pacchetti dell'applicazione con Visual Studio. Per altre informazioni, vedere creare [un pacchetto di un'app UWP con Visual Studio](/windows/msix/package/packaging-uwp-apps).

Il Microsoft Store semplifica la creazione, l'invio e la vendita di app per i clienti di tutto il mondo. Per altre informazioni, vedere [invii di app](/windows/uwp/publish/app-submissions).

I cmdlet di Windows PowerShell consentono di installare e gestire app di Windows line-of-business senza usare lo Store. Per altre informazioni, vedere [cmdlet del modulo appx](/powershell/module/appx/index?view=win10-ps).

Usando le API di creazione di pacchetti, distribuzione e query, è possibile eseguire queste attività a livello di codice:

-   Creare un pacchetto dell'app per un'app di Windows
-   Distribuire un'app di Windows in pacchetto
-   Enumerare i pacchetti dell'app installati in un sistema e ottenere informazioni su di essi dal relativo manifesto
-   Utilizzare il contenuto di un pacchetto dell'app

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                    | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come creare un pacchetto di app (C++)](how-to-create-a-package.md)                                        | Informazioni su come creare un pacchetto dell'app usando l'API per la creazione di pacchetti.                                                                                                                           |
| [Come creare un certificato di firma del pacchetto di un'app](how-to-create-a-package-signing-certificate.md)      | Informazioni su come usare [**Makecert**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) per creare un certificato di firma del codice di test, in modo che sia possibile firmare i pacchetti dell'applicazione. |
| [Come firmare un pacchetto di app con SignTool](how-to-sign-a-package-using-signtool.md)                    | Informazioni su come usare [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti dell'app in modo che possano essere distribuiti.                                                                    |
| [Come risolvere gli errori di firma del pacchetto dell'app](how-to-troubleshoot-app-package-signature-errors.md) | Un errore di distribuzione dell'app può essere causato da un errore di convalida della firma digitale del pacchetto dell'app. Informazioni su come riconoscere questi errori e su come eseguirli.          |
| [Come firmare un pacchetto dell'applicazione a livello di codice (C++)](how-to-programmatically-sign-a-package.md)          | Informazioni su come firmare un pacchetto dell'app usando la funzione [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .                                                                                   |
| [Come sviluppare un'app OEM che usa un file personalizzato](how-to-develop-oem-app-with-custom-file.md)         | Informazioni su come sviluppare un'app che usa un file personalizzato per passare le informazioni dall'OEM all'app.                                                                                             |
| [Estrarre il contenuto del pacchetto dell'app (C++)](how-to-extract-content-from-a-package.md)                          | Informazioni su come estrarre i file da un pacchetto dell'app usando l'API per la creazione di pacchetti.                                                                                                               |
| [Informazioni sul manifesto del pacchetto dell'applicazione di query (C++)](how-to-query-package-identity-information.md)                   | Informazioni su come ottenere informazioni da un manifesto del pacchetto dell'app usando l'API per la creazione di pacchetti                                                                                                            |
| [Risoluzione dei problemi](troubleshooting.md)                                                                   | Fornisce informazioni utili per la risoluzione dei problemi che si verificano durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto dell'app.                                                                 |
| [Informazioni di riferimento sulle API di creazione pacchetti](interfaces.md)                                                                | L'API di creazione pacchetti crea, legge e scrive i pacchetti dell'app.                                                                                                                            |
| [Informazioni di riferimento sulle API di distribuzione](package-deployment-api.md)                                                   | L'API di distribuzione installa, aggiorna e Disinstalla i pacchetti dell'app.                                                                                                                    |
| [Riferimento all'API di query](functions.md)                                                                     | L'API di query ottiene informazioni sui pacchetti dell'applicazione installati nel sistema.                                                                                                               |
| [Strumenti e cmdlet di PowerShell](appx-packaging-tools.md)                                                 | Usare questi strumenti e cmdlet per creare, installare e gestire i pacchetti dell'applicazione.                                                                                                              |
| [Esempi di SDK](appx-packaging-samples.md)                                                                | Scaricare esempi di SDK che illustrano le API per la creazione di pacchetti, la distribuzione e le query per le app di Windows.                                                                               |
| [Glossario](appx-packaging-glossary.md)                                                                  | Informazioni sui termini correlati a creazione di pacchetti, distribuzione e query delle app di Windows.                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Concetti**
</dt> <dt>

[Distribuzione e pacchetti dell'applicazione](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Altri riferimenti**
</dt> <dt>

[Schema del manifesto del pacchetto dell'applicazione](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel. Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel. PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 