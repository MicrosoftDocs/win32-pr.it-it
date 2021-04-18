---
title: Come sviluppare un'app OEM che usa un file personalizzato
description: Informazioni su come sviluppare un'app che usa un file personalizzato per passare le informazioni dall'OEM all'app.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299588"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Come sviluppare un'app OEM che usa un file personalizzato

Per altre informazioni sulla creazione e l'uso di file di dati personalizzati, vedere [Opzioni di Command-Line manutenzione del pacchetto dell'app DISM (con estensione appx o appxbundle)](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Informazioni su come sviluppare un'app che usa un file personalizzato per passare le informazioni dall'OEM all'app.

Per le app create per la distribuzione OEM, è possibile usare un file personalizzato per passare le informazioni dall'OEM alle app. Per passare le informazioni OEM a un'app, creare un file. data personalizzato nella cartella microsoft.system. Package. Metadata. Questo nome file è speciale per il sistema operativo e viene eseguito automaticamente durante gli aggiornamenti del sistema operativo. Gli OEM possono usare questo file per passare gli identificatori personalizzati, in modo che le app sappiano quando gli OEM li hanno distribuiti. È possibile avere un solo file. data personalizzato per app. Le app devono essere in grado di cercare e leggere correttamente questo file. Gli sviluppatori considerano il file come dati non attendibili.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Guida introduttiva: informazioni sul manifesto del pacchetto dell'app](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Prerequisiti

-   Per aggiungere il pacchetto dell'app con il file di dati personalizzato, è necessario lo strumento [gestione e manutenzione immagini distribuzione (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) .

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Passaggio 1: creare un file personalizzato e aggiungerlo alla cartella dei metadati del pacchetto

È possibile progettare l'applicazione in modo da usare qualsiasi formato scelto per i dati personalizzati. È ad esempio possibile usare XML, un file di testo o un altro tipo di file per organizzare i dati. Si consiglia di considerare come è possibile testare e convalidare il file. Ad esempio, è possibile creare un XML Schema per convalidare un file XML.

È possibile specificare qualsiasi tipo di file con qualsiasi nome file per i dati personalizzati. Quando si aggiunge il pacchetto dell'app con il file di dati personalizzato utilizzando lo strumento [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , DISM Rinomina il file personalizzato in Custom. Data e lo salva nella cartella microsoft.system. Package. Metadata.

> [!Note]  
> Il file di dati personalizzato non può essere modificato dall'app. Si tratta di una risorsa di sola lettura.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Passaggio 2: accedere al file di dati personalizzato per un'app

È possibile accedere al file Custom. Data per un'app dal codice usando le API di Windows per ottenere informazioni per il pacchetto corrente. Ad esempio:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Per altre informazioni sullo sviluppo con la proprietà [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , vedere [Guida introduttiva: informazioni sul manifesto del pacchetto dell'app](how-to-query-package-identity-information.md).

Per ulteriori informazioni sull'accesso al file Custom. Data tramite [**IStorageFolder. getFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) e l'utilizzo di oggetti [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , vedere [accesso a dati e file](/previous-versions/windows/apps/hh464959(v=win.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida introduttiva: informazioni sul manifesto del pacchetto dell'app](how-to-query-package-identity-information.md)
</dt> </dl>

 

 