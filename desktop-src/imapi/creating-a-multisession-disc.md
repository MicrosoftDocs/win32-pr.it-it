---
title: Creazione di un disco multisessione
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'Altre informazioni su: creazione di un disco a più sessioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485436"
---
# <a name="creating-a-multisession-disc"></a>Creazione di un disco multisessione

L'API per la creazione di [Immagini Master](about-imapi.md) (IMAPI) supporta l'aggiunta e la rimozione di file da e verso i seguenti tipi di dischi multisessione:

-   CD-R/CD-RW
-   Single-Layer DVD + R/DVD-R
-   DVD + R Dual Layer
-   BD-R
-   DVD-RW/DVD + RW (**solo Windows 7**)
-   DVD-RAM (**solo Windows 7**)
-   BD-RE (**solo Windows 7**)

La creazione di un disco a più sessioni con IMAPi prevede i passaggi seguenti. Ognuno di questi passaggi documentati contiene la parte pertinente dell'esempio di script completo Visual Basic disponibile nella sezione finale.

## <a name="initializing-the-disc-recorder"></a>Inizializzazione del registratore di dischi

Prima dell'inizializzazione del dispositivo, l'oggetto **MsftDiscMaster2** fornisce un'enumerazione dei dispositivi ottici nel sistema. L'interfaccia [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornisce l'accesso a questa enumerazione del dispositivo per facilitare la posizione del dispositivo di registrazione appropriato. L'oggetto **MsftDiscMaster2** fornisce anche le notifiche degli eventi quando i dispositivi ottici vengono aggiunti o rimossi da un computer.

Dopo aver individuato un registratore ottico e aver recuperato l'ID assegnato, creare un nuovo oggetto **MsftDiscMaster2** e inizializzare il registratore usando l'ID dispositivo specifico.

L'interfaccia [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) consente di accedere alle informazioni di base sul dispositivo, ad esempio ID fornitore, ID prodotto, revisione del prodotto, nonché i metodi per estrarre i supporti o chiudere la barra.

> [!Note]  
> Le costanti e le dimensioni aggiuntive dichiarate nell'esempio seguente vengono usate in un secondo momento nello script di esempio completo presente nella sezione finale di questo documento. Questi elementi non sono necessari per l'operazione di inizializzazione di un registratore di dischi.

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a>Creazione di un writer di dati

L'oggetto _ *MsftDiscFormat2Data** fornisce il metodo di scrittura, le relative proprietà e le proprietà specifiche del supporto. L'interfaccia [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornisce l'accesso a questo oggetto.

La registrazione del disco viene associata al writer del formato utilizzando la proprietà [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Dopo che il registratore è stato associato al writer di formato, è possibile eseguire query sui supporti e sulle proprietà specifiche della scrittura prima di scrivere l'immagine del risultato nel disco usando il metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

> [!Note]  
> La stringa del nome client specificata nel codice di esempio riportato di seguito deve essere regolata in base alle esigenze dell'applicazione specifica.

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>Creazione dell'oggetto file System

Per registrare una nuova sessione, prima di tutto è necessario generare un'immagine di masterizzazione. Un'immagine Burn per i formati **ISO9660**, **Joliet** e **UDF** è costituita da file System di singoli file e directory. L'oggetto **MsftFileSystemImage** è l'oggetto file system contenente i file e le directory da collocare sul supporto ottico. L'interfaccia [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornisce l'accesso all'oggetto file System e alle impostazioni.


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>Importazione di un file System

Prima di procedere, verificare che il disco non sia vuoto controllando la proprietà [**IDiscFormat2:: Get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .

Dopo aver creato l'oggetto **MsftFileSystemImage** , la proprietà [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) deve essere inizializzata prima di una chiamata al metodo [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) o [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) per importare il file System dall'ultima sessione registrata. Questi metodi compileranno automaticamente l'oggetto **MsftFileSystemImage** con le informazioni che descrivono i file e le directory precedentemente registrati.

> [!Note]  
> La proprietà [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) viene in genere inizializzata con le interfacce multisessione fornite dal writer di dati tramite la proprietà [**IDiscFormat2Data:: Get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .

 

Il tentativo di impostare la proprietà **IFileSystemImage::p UT \_ MultisessionInterfaces** avrà esito negativo se IMAPI non supporta la multisessione per il supporto attualmente inserito o se non è possibile accodare il supporto per altri motivi, ad esempio perché è chiuso.

Se la sessione Burn precedente conteneva più di un tipo di file system, il metodo [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importerà le informazioni del tipo di file System più avanzato presente. Ad esempio, nell'esempio fornito in questo argomento, UDF è il file system importato. Tuttavia, l'utilizzo del metodo [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) consente la selezione specifica del file System da importare.

> [!Note]  
> Il metodo [**IFileSystemImage:: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) può essere usato per determinare quali file System sono disponibili nel disco.

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a>Aggiunta o rimozione di file nel file System

Dopo aver creato l'oggetto file system e aver importato i file system dalla sessione precedente, chiamare i metodi [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) per creare nuovi oggetti di file e directory, rispettivamente. Gli oggetti file e directory forniscono dettagli specifici sui file e le directory. In alternativa, è possibile usare il metodo [**metodo IFsiDirectoryItem:: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) di un oggetto directory, rappresentato tramite l'interfaccia [**metodo IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , per aggiungere file e directory esistenti da un altro dispositivo di archiviazione (ad esempio un disco rigido).

Il metodo di aggiornamento del gestore eventi disponibile per [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifica il file corrente da aggiungere all'immagine file System, il numero di settori già copiati e il numero totale di settori da copiare.

Per rimuovere i file e le directory esistenti dalla file system, usare i metodi [**metodo IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**metodo IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) degli oggetti directory rappresentati tramite l'interfaccia [**metodo IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) . La proprietà [**IFileSystemImage:: Get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) viene utilizzata per ottenere un puntatore alla directory radice del file System e l'interfaccia **metodo IFsiDirectoryItem** per attraversare l'albero di directory.

> [!Note]  
> I file e le directory rimossi tramite i metodi [**metodo IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**metodo IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) non vengono rimossi fisicamente dal disco e il software avanzato può recuperare facilmente le informazioni eliminate.

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>Creazione di un'immagine del file System

Il passaggio finale consiste nel chiamare [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) per creare un flusso di dati per l'immagine Burn e fornire l'accesso tramite l'interfaccia [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) . Questo flusso di dati può essere fornito direttamente al metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) oppure deve essere salvato in un file per un uso successivo.


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>Riepilogo di esempio

Nell'esempio di script Visual Basic riportato di seguito viene illustrato come utilizzare gli oggetti IMAPi per creare dischi multisessione. Nell'esempio viene creata una nuova sessione e viene aggiunta una directory al disco. Per semplicità, il codice non esegue un controllo degli errori esteso e presuppone quanto segue:

-   Nel sistema è installato un dispositivo disco compatibile.
-   Il dispositivo disco è la prima unità nel sistema.
-   Viene inserito un disco compatibile nel dispositivo disco.
-   I file da aggiungere al disco si trovano in "g: \\ burndir".

È possibile aggiungere allo script funzionalità aggiuntive, ad esempio il controllo completo degli errori, la compatibilità di dispositivi e supporti, la notifica degli eventi e il calcolo dello spazio disponibile sul disco.


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPi](using-imapi.md)
</dt> <dt>

[_ *IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
