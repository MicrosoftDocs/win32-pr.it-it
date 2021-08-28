---
title: Interfacce IMAPI
description: Le tabelle seguenti identificano e descrivono brevemente le interfacce usate dagli sviluppatori C/C++ e l'oggetto di scripting associato. Antefisci il nome dell'oggetto nella tabella con \ 0034;IMAPI2. \ 0034; per qualificare completamente il nome dell'oggetto durante la creazione dell'oggetto nello script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c093acd587f975859d68fda23f6c1f169d969a78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466178"
---
# <a name="imapi-interfaces"></a>Interfacce IMAPI

Le tabelle seguenti identificano e descrivono brevemente le interfacce usate dagli sviluppatori C/C++ e l'oggetto di scripting associato. Antefisci il nome dell'oggetto nella tabella con "IMAPI2". per qualificare completamente il nome dell'oggetto durante la creazione dell'oggetto nello script.

Nella tabella seguente sono elencate le interfacce associate ai dispositivi, il motore di masterizzazione e i writer di formato e la gomma.




| | | Interfaccia | Oggetto | | Motore di masterizzazione di basso livello.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li></ul> | MsftWriteEngine2 | | Writer di immagini principale.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li></ul> | Oggetto MsftDiscFormat2Data | | Gomma da disco.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li></ul> | MsftDiscFormat2Erase | | Writer di immagini non elaborato.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li></ul> | MsftDiscFormat2RawCD | | Writer di immagini Track-At-Once.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li></ul> | MsftDiscFormat2TrackAtOnce | | Enumerazione dei dispositivi disco nell'elenco dell'hardware di sistema.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li></ul> | MsftDiscMaster2 | | Delegato di notifica per l'oggetto MsftDiscMaster2.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li></ul> | DDiscMaster2Events | | Singolo dispositivo di registrazione.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li></ul> | MsftDiscRecorder2 | | Attributi di scrittura del dispositivo, inclusi il tipo di supporto, la velocità di scrittura e il tipo di controllo della velocità angolare.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li></ul> | MsftWriteSpeedDescriptor | 




 

Nella tabella seguente sono elencate le file system seguenti.




| | | Interfaccia | Oggetto | | Flusso dell'immagine d'avvio e proprietà per l'integrazione dell'immagine di avvio nell'immagine del disco.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li></ul> | AvvioOpzioni | | Immagine e proprietà del file system. Questo oggetto include tutte le tracce e i riferimenti all'immagine d'avvio e all'immagine del risultato.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li></ul> | CFileSystemImage | | Contenitore del flusso di dati fornito dall'oggetto file system dati.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li></ul> | FileSystemImageResult | | Elemento directory nell'immagine file system personalizzata.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li></ul> | FsiDirectoryItem | | Elemento file nell'immagine file system personalizzata.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li></ul> | FsiFileItem | | Interfaccia contenente le proprietà comuni agli elementi di file e directory.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li></ul> | FsiItem | | Creazione di un'immagine CD RAW.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li></ul> | MsftRawCDImageCreator | | Oggetto helper oggetto stream per concatenare più flussi.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li></ul> | MsftStreamConcatenate | | Flusso interleaved da aggiungere all'immagine del disco.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li></ul> | MsftStreamInterleave | | Flusso generato pseudo-casuale.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li></ul> | MsftStreamPrgn001 | | L'oggetto di scripting <strong>MsftStreamZero</strong> non viene implementato come interfaccia. | <a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a> | 




 

Nella tabella seguente sono elencate le interfacce helper.




| | | Interfaccia | Oggetto | | Raccolta di intervalli di settori all'interno di file system immagine.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li></ul> | Nessun oggetto corrispondente | | Supporto per la verifica della masterizzazione.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>I Riunificazione</strong></a></li></ul> | Nessun oggetto corrispondente | | Enumeratore di FsiItems per applicazioni C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li></ul> | EnumFsiItems | | Enumeratore di ProgressItems per applicazioni C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li></ul> | EnumProgressItems | | <ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li></ul> | FsiFileItem2 supporta | | verifica dell'immagine iso.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li></ul> | Nessun oggetto corrispondente | | Supporto di più sessioni.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li></ul> | Nessun oggetto corrispondente | | Supporto sequenziale di più sessioni.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li></ul> | MsftMultisessionSequential | | Nome del file e blocchi associati nell'immagine del risultato.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li></ul> | Oggetto ProgressItem | | Elenco di immagini dei risultati, suddiviso in base al nome file e ai blocchi associati.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li></ul> | Oggetto ProgressItems | 




 

 

 




