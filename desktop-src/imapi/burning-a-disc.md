---
title: Masterizzazione di un'immagine disco
description: "La masterizzazione (masterizzazione di un disco) tramite IMAPI è costituita dai passaggi seguenti: Costruire un'immagine file system che contiene le directory e i file per scrivere il disco. Configurare un registratore di dischi per comunicare con il dispositivo ottico. Creare un writer di dati e masterizzare l'immagine su disco."
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237a4aa73b6820b75b4a9a1ed03baeeb87ac093bfc549cb9cc0ed947077515dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758911"
---
# <a name="burning-a-disc-image"></a>Masterizzazione di un'immagine disco

La masterizzazione (masterizzazione di un disco) tramite IMAPI è costituita dai passaggi seguenti:

1.  Costruire un file system che contiene le directory e i file per scrivere il disco.
2.  [Configurare un registratore di dischi](#set-up-a-disc-recorder) per comunicare con il dispositivo ottico.
3.  [Creare un writer di dati](#create-a-data-writer-and-write-the-burn-image) e masterizzare l'immagine su disco.

Per un esempio che masterizza un'immagine disco, vedere [Esempio di VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Costruire un'immagine di masterizzazione

Un'immagine di masterizzazione è un flusso di dati pronto per la scrittura su supporti ottici. L'immagine di masterizzazione per i formati ISO9660, Joliet e UDF è costituita da file system di singoli file e directory. **L'oggetto CFileSystemImage** è file system che contiene i file e le directory da posizionare sul supporto ottico. [**L'interfaccia IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornisce l'accesso all'oggetto file system e alle impostazioni.

Dopo aver creato l'oggetto file system, chiamare rispettivamente i metodi [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) per creare rispettivamente gli oggetti file e directory. Gli oggetti file e directory possono essere usati per fornire dettagli specifici sul file e sulla directory. I metodi del gestore eventi disponibili per [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) possono identificare il file corrente aggiunto all'immagine file system, il numero di settori già copiati e il numero totale di settori da copiare.

Facoltativamente, un'immagine d'avvio può essere collegata al file system usando la proprietà [**IFileSystemImage::p ut \_ BootImageOptions.**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) Per un esempio, vedere [Aggiunta di un'immagine d'avvio](adding-a-boot-image.md).

Chiamare infine [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) per creare un flusso di dati e fornisce l'accesso tramite [**IFileSystemImageResult.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) Il nuovo flusso di dati può quindi essere fornito direttamente al metodo [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) o salvato in un file per un uso successivo.

## <a name="set-up-a-disc-recorder"></a>Configurare un registratore di dischi

**L'oggetto MsftDiscMaster2** fornisce un'enumerazione dei dispositivi ottici nel sistema. [**L'interfaccia IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornisce l'accesso all'enumerazione del dispositivo risultante. Attraversare le enumerazioni per individuare un dispositivo di registrazione appropriato. **L'oggetto MsftDiscMaster2** fornisce anche notifiche degli eventi quando i dispositivi ottici vengono aggiunti o eliminati da un computer.

Dopo aver trovato un registratore ottico e averne recuperato l'ID, creare un **oggetto MsftDiscRecorder2** e inizializzare il registratore usando l'ID dispositivo. [**L'interfaccia IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornisce l'accesso all'oggetto registratore, nonché ad alcune informazioni di base sul dispositivo, ad esempio l'ID fornitore, l'ID prodotto, la revisione del prodotto e i metodi per espellere il supporto e chiudere il vassoio.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Creare un writer di dati e scrivere l'immagine di masterizzazione

**L'oggetto MsftDiscFormat2Data** fornisce il metodo di scrittura, le proprietà relative alla funzione di scrittura e le proprietà specifiche dei supporti. [**L'interfaccia IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) consente di accedere all'oggetto **MsftDiscFormat2Data.**

Il registratore di dischi si collega al writer di formato usando la [**proprietà IDiscFormat2Data::p ut \_ Recorder.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) Dopo aver associato il registratore al writer di formato, è possibile eseguire query relative ai supporti e aggiornare le proprietà specifiche della scrittura prima di scrivere l'immagine del risultato su disco usando il metodo [**IDiscFormat2Data::Write.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write)

Altre interfacce di scrittura del formato fornite da IMAPI funzionano in modo analogo. Altre interfacce di scrittura del formato includono:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) cancella i supporti ottici risibile.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) scrive un'immagine non elaborata nei supporti ottici.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) scrive tracce audio in supporti ottici.

> [!Note]  
> È possibile che una transizione dello stato di alimentazione si ssegni durante un'operazione di masterizzazione ,ad esempio la disconnessione dell'utente o la sospensione del sistema, che causa l'interruzione del processo di masterizzazione e la possibile perdita di dati. Per considerazioni sulla programmazione, vedere [Prevenzione della disconnessione o sospensione durante una masterizzazione.](preventing-logoff-or-suspend-during-a-burn.md)

 

## <a name="vbscript-example"></a>Esempio di VBScript

Questo esempio di script illustra come usare gli oggetti IMAPI per masterizzare supporti ottici. in particolare, scrivere una directory in un disco vuoto. Il codice non contiene alcun controllo degli errori e presuppone quanto segue:

-   Nel sistema è installato un dispositivo disco compatibile.
-   Il dispositivo disco è la seconda unità del sistema.
-   Nel dispositivo disco viene inserito un disco compatibile.
-   Il disco è vuoto.
-   I file da scrivere su disco si trovano in "g: \\ burndir".

È possibile aggiungere a questo script funzionalità aggiuntive come il controllo degli errori, la compatibilità di dispositivi e supporti, la notifica degli eventi e il calcolo dello spazio disponibile sul disco.


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

[Uso di IMAPI](using-imapi.md)
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

[**Istream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 