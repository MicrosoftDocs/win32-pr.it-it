---
title: Come sviluppare un'app OEM che usa un file personalizzato
description: Informazioni su come sviluppare un'app che usa un file personalizzato per passare informazioni dall'OEM all'app.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780e930d057c325038c94dc86fc375c70bdb1cc8dca34ac6169436bc0f0e323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855321"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Come sviluppare un'app OEM che usa un file personalizzato

Per altre informazioni sulla creazione e sull'uso di file di dati personalizzati, vedere [DiSM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Informazioni su come sviluppare un'app che usa un file personalizzato per passare informazioni dall'OEM all'app.

Per le app create per la distribuzione OEM, è possibile usare un file personalizzato per passare informazioni dall'OEM alle app. Per passare informazioni OEM a un'app, creare un file Custom.data nella microsoft.system.package.metadata. Questo nome file è speciale per il sistema operativo e viene automaticamente portato avanti durante gli aggiornamenti del sistema operativo. Gli OEM possono usare questo file per passare identificatori personalizzati, in modo che le app sappiano quando gli OEM li hanno distribuiti. È possibile avere un solo file Custom.data per ogni app. Le app devono essere in grado di cercare e leggere correttamente questo file. Gli sviluppatori trattano il file come dati non attendibili.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Guida introduttiva: Eseguire query sulle informazioni sul manifesto del pacchetto dell'app](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Prerequisiti

-   È necessario lo [strumento Gestione e manutenzione immagini distribuzione (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) per aggiungere il pacchetto dell'app con il file di dati personalizzato.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Passaggio 1: Creare un file personalizzato e aggiungerlo alla cartella dei metadati del pacchetto

È possibile progettare l'app in modo che usi qualsiasi formato scelto per i dati personalizzati. Ad esempio, è possibile usare XML, un file di testo o un altro tipo di file per organizzare i dati. È consigliabile valutare come testare e convalidare il file. Ad esempio, è possibile creare uno schema XML per convalidare un file XML.

È possibile specificare qualsiasi tipo di file con qualsiasi nome file per i dati personalizzati. Quando si aggiunge il pacchetto dell'app [](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) con il file di dati personalizzato usando lo strumento Gestione e manutenzione immagini distribuzione, il file personalizzato viene rinominato in Custom.data e salvato nella cartella microsoft.system.package.metadata.

> [!Note]  
> Il file di dati personalizzato non può essere modificato dall'app. Si tratta di una risorsa di sola lettura.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Passaggio 2: Accedere al file di dati personalizzato per un'app

È possibile accedere al file Custom.data per un'app dal codice usando le API Windows per ottenere informazioni per il pacchetto corrente. Esempio:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Per altre informazioni sullo sviluppo con la [**proprietà Package.Current,**](/uwp/api/windows.applicationmodel.package.current) vedere Guida introduttiva: Eseguire query sulle informazioni sul manifesto [del pacchetto dell'app.](how-to-query-package-identity-information.md)

Per altre informazioni sull'accesso al file custom.data tramite [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) e sull'uso di oggetti [**StorageFile,**](/uwp/api/Windows.Storage.StorageFile) vedere [Accesso a dati e file.](/previous-versions/windows/apps/hh464959(v=win.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida introduttiva: Eseguire query sulle informazioni sul manifesto del pacchetto dell'app](how-to-query-package-identity-information.md)
</dt> </dl>

 

 