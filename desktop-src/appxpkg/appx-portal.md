---
title: Creazione di pacchetti, distribuzione ed esecuzione di query Windows app
description: Creare pacchetti di app a livello di Windows e installare, aggiornare, eseguire query e disinstallare i pacchetti dell'app.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814274"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Creazione di pacchetti, distribuzione ed esecuzione di query Windows app

È possibile distribuire, gestire e gestire app Windows (inclusi UWP e app desktop) tramite pacchetti di app msix/.appx basati sul formato OPC. Ogni pacchetto dell'app contiene i file che costituiscono l'app e un file manifesto che descrive il software da Windows.

## <a name="introduction"></a>Introduzione

In genere, gli sviluppatori creano e firmano pacchetti di app usando Visual Studio. Per altre informazioni, vedi [Creare un pacchetto di un'app UWP con Visual Studio](/windows/msix/package/packaging-uwp-apps).

Il Microsoft Store semplifica la creazione, l'invio e la vendita delle app ai clienti di tutto il mondo. Per altre informazioni, vedere [Invii di app.](/windows/uwp/publish/app-submissions)

Windows PowerShell cmdlet consentono di installare e gestire app line-of-business Windows senza usare lo Store. Per altre informazioni, vedere [Cmdlet del modulo Appx.](/powershell/module/appx/index?view=win10-ps)

Usando le API per la creazione di pacchetti, la distribuzione e le query, è possibile eseguire queste attività a livello di codice:

-   Creare un pacchetto dell'app per un Windows app
-   Distribuire un'app Windows pacchetto
-   Enumerare i pacchetti dell'app installati in un sistema e ottenere informazioni su di essi dal manifesto
-   Utilizzare il contenuto di un pacchetto dell'app

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                    | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come creare un pacchetto di app (C++)](how-to-create-a-package.md)                                        | Informazioni su come creare un pacchetto dell'app usando l'API di creazione pacchetti.                                                                                                                           |
| [Come creare un certificato di firma del pacchetto di un'app](how-to-create-a-package-signing-certificate.md)      | Informazioni su come usare [**MakeCert**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) per creare un certificato di firma del codice di test per poter firmare i pacchetti dell'app. |
| [Come firmare un pacchetto di app con SignTool](how-to-sign-a-package-using-signtool.md)                    | Informazioni su come usare [**SignTool per**](/windows-hardware/drivers/devtest/signtool) firmare i pacchetti dell'app in modo che possano essere distribuiti.                                                                    |
| [Come risolvere gli errori di firma del pacchetto dell'app](how-to-troubleshoot-app-package-signature-errors.md) | Un errore di distribuzione dell'app può essere causato da un errore di convalida della firma digitale del pacchetto dell'app. Informazioni su come riconoscere questi errori e su come procedere.          |
| [Come firmare un pacchetto dell'app a livello di codice (C++)](how-to-programmatically-sign-a-package.md)          | Informazioni su come firmare un pacchetto dell'app usando la [**funzione SignerSignEx2.**](/windows/desktop/SecCrypto/signersignex2)                                                                                   |
| [Come sviluppare un'app OEM che usa un file personalizzato](how-to-develop-oem-app-with-custom-file.md)         | Informazioni su come sviluppare un'app che usa un file personalizzato per passare informazioni dall'OEM all'app.                                                                                             |
| [Estrarre il contenuto del pacchetto dell'app (C++)](how-to-extract-content-from-a-package.md)                          | Informazioni su come estrarre file da un pacchetto dell'app usando l'API di creazione pacchetti.                                                                                                               |
| [Eseguire query sulle informazioni sul manifesto del pacchetto dell'app (C++)](how-to-query-package-identity-information.md)                   | Informazioni su come ottenere informazioni da un manifesto del pacchetto dell'app usando l'API di creazione pacchetti                                                                                                            |
| [Risoluzione dei problemi](troubleshooting.md)                                                                   | Fornisce informazioni che consentono di risolvere i problemi che si verificano durante la creazione di pacchetti, la distribuzione o l'esecuzione di query su un pacchetto dell'app.                                                                 |
| [Informazioni di riferimento sulle API di creazione pacchetti](interfaces.md)                                                                | L'API per la creazione di pacchetti crea, legge e scrive pacchetti dell'app.                                                                                                                            |
| [Informazioni di riferimento sulle API di distribuzione](package-deployment-api.md)                                                   | L'API di distribuzione installa, aggiorna e disinstalla i pacchetti dell'app.                                                                                                                    |
| [Informazioni di riferimento sulle API di query](functions.md)                                                                     | L'API di query ottiene informazioni sui pacchetti dell'app installati nel sistema.                                                                                                               |
| [Strumenti e cmdlet di PowerShell](appx-packaging-tools.md)                                                 | Usare questi strumenti e cmdlet per creare, installare e gestire i pacchetti dell'app.                                                                                                              |
| [Esempi di SDK](appx-packaging-samples.md)                                                                | Scaricare esempi di SDK che illustrano le API di creazione di pacchetti, distribuzione e query per Windows app.                                                                               |
| [Glossario](appx-packaging-glossary.md)                                                                  | Informazioni sui termini relativi alla creazione di pacchetti, alla distribuzione e alle query Windows app.                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Concetti**
</dt> <dt>

[Pacchetti di app e distribuzione](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Altri riferimenti**
</dt> <dt>

[Schema del manifesto del pacchetto dell'applicazione](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel.Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel.PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 