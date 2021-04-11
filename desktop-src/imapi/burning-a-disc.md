---
title: Masterizzazione di un'immagine del disco
description: La creazione di un disco con IMAPi è costituita dai passaggi seguenti per creare un'immagine di file system contenente le directory e i file per la scrittura del disco. Configurare un registratore di dischi per comunicare con il dispositivo ottico. Creare un writer di dati e masterizzare l'immagine su disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337191"
---
# <a name="burning-a-disc-image"></a>Masterizzazione di un'immagine del disco

La Master (Burning a Disk) con IMAPi prevede i passaggi seguenti:

1.  Costruire un'immagine di file system contenente le directory e i file da scrivere nel disco.
2.  [Configurare un registratore di dischi](#set-up-a-disc-recorder) per comunicare con il dispositivo ottico.
3.  [Creare un writer di dati](#create-a-data-writer-and-write-the-burn-image) e masterizzare l'immagine su disco.

Per un esempio in cui viene bruciata un'immagine del disco, vedere l' [esempio VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Costruire un'immagine di masterizzazione

Un'immagine Burn è un flusso di dati pronto per essere scritto su supporti ottici. L'immagine Burn per i formati ISO9660, Joliet e UDF è costituita da una file system di singoli file e directory. L'oggetto **CFileSystemImage** è l'oggetto file System che include i file e le directory da collocare sul supporto ottico. L'interfaccia [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornisce l'accesso all'oggetto file System e alle impostazioni.

Dopo aver creato l'oggetto file system, chiamare i metodi [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) per creare rispettivamente gli oggetti file e directory. È possibile utilizzare gli oggetti file e directory per fornire dettagli specifici sul file e sulla directory. I metodi del gestore eventi disponibili per [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) possono identificare il file corrente da aggiungere all'immagine file System, il numero di settori già copiati e il numero totale di settori da copiare.

Facoltativamente, un'immagine di avvio può essere collegata al file system usando la proprietà [**IFileSystemImage::p UT \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) . Per un esempio, vedere [aggiunta di un'immagine di avvio](adding-a-boot-image.md).

Infine, chiamare [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) per creare un flusso di dati e fornire l'accesso tramite [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). Il nuovo flusso di dati può quindi essere fornito direttamente al metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) oppure essere salvato in un file per un uso successivo.

## <a name="set-up-a-disc-recorder"></a>Configurare un registratore di dischi

L'oggetto **MsftDiscMaster2** fornisce un'enumerazione dei dispositivi ottici nel sistema. L'interfaccia [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornisce l'accesso all'enumerazione dei dispositivi risultante. Attraversare le enumerazioni per individuare un dispositivo di registrazione appropriato. L'oggetto **MsftDiscMaster2** fornisce anche le notifiche degli eventi quando i dispositivi ottici vengono aggiunti o eliminati da un computer.

Dopo aver individuato un registratore ottico e aver recuperato il relativo ID, creare un oggetto **MsftDiscRecorder2** e inizializzare il registratore usando l'ID del dispositivo. L'interfaccia [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornisce l'accesso all'oggetto registratore, oltre ad alcune informazioni di base sul dispositivo, ad esempio ID fornitore, ID prodotto, revisione del prodotto e metodi per estrarre il supporto e chiudere la barra.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Creare un writer di dati e scrivere l'immagine di masterizzazione

L'oggetto **MsftDiscFormat2Data** fornisce il metodo di scrittura, le proprietà relative alla funzione Write e alle proprietà specifiche del supporto. L'interfaccia [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornisce l'accesso all'oggetto **MsftDiscFormat2Data** .

La registrazione del disco è collegata al writer del formato usando la proprietà [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Dopo che il registratore è stato associato al writer di formato, è possibile eseguire query relative ai supporti e aggiornare le proprietà specifiche della scrittura prima di scrivere l'immagine del risultato in un disco usando il metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

Altre interfacce di scrittura del formato fornite da IMAPi funzionano in modo analogo; le interfacce aggiuntive per la scrittura di formati includono:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) Cancella i supporti ottici riscrivibili.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) scrive un'immagine non elaborata in un supporto ottico.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) scrive tracce audio su supporti ottici.

> [!Note]  
> È possibile che si verifichi una transizione di stato dell'alimentazione durante un'operazione di masterizzazione, ad esempio la disconnessione dell'utente o la sospensione del sistema, che comporta l'interruzione del processo di masterizzazione e la possibile perdita di dati. Per considerazioni sulla programmazione, vedere [Impedisci la disconnessione o la sospensione durante un'ustione](preventing-logoff-or-suspend-during-a-burn.md).

 

## <a name="vbscript-example"></a>Esempio di VBScript

Questo esempio di script Mostra come usare gli oggetti IMAPi per masterizzare supporti ottici; in particolare, scrivere una directory in un disco vuoto. Il codice non contiene alcun controllo degli errori e presuppone quanto segue:

-   Nel sistema è installato un dispositivo disco compatibile.
-   Il dispositivo disco è la seconda unità del sistema.
-   Viene inserito un disco compatibile nel dispositivo disco.
-   Il disco è vuoto.
-   I file da scrivere sul disco si trovano in "g: \\ burndir".

A questo script è possibile aggiungere funzionalità aggiuntive, ad esempio il controllo degli errori, la compatibilità di dispositivi e supporti, la notifica degli eventi e il calcolo dello spazio disponibile sul disco.


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPi](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 