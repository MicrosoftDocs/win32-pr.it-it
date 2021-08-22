---
title: Informazioni sul monitoraggio delle cartelle
description: Informazioni sul monitoraggio delle cartelle
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, monitoraggio delle cartelle
- Windows Media Player a oggetti, monitoraggio delle cartelle
- modello a oggetti, monitoraggio delle cartelle
- Windows Media Player ActiveX, monitoraggio delle cartelle
- ActiveX controllo, monitoraggio delle cartelle
- Windows Media Player Controllo ActiveX per dispositivi mobili, monitoraggio delle cartelle
- Windows Media Player Dispositivi mobili, monitoraggio delle cartelle
- monitoraggio delle cartelle
- cartelle di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1206defcdc387659567ceedcf7347a3ab99ca45d9926a9bd32c4f75280a8a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055509"
---
# <a name="about-folder-monitoring"></a>Informazioni sul monitoraggio delle cartelle

Windows Media Player possibile monitorare le cartelle che contengono file multimediali digitali e aggiornare la libreria quando i file vengono aggiunti o rimossi. Questa funzionalità di monitoraggio delle cartelle viene fornita [dall'interfaccia IWMPFolderMonitorServices.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

Per usare i servizi di monitoraggio delle cartelle, è necessario creare l'oggetto Player in uno stato remoto. Per altre informazioni sulla comunicazione remota, vedere [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md). Dopo aver creato un'istanza remota del lettore, ottenere un puntatore **all'interfaccia IWMPFolderMonitorServices** chiamando **QueryInterface** sull'interfaccia [IWMPPlayer.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)

Windows Media Player un elenco di cartelle monitorate. Per ottenere un elenco di cartelle monitorate, usare i [metodi IWMPFolderMonitorServices::get \_ e](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) [IWMPFolderMonitorServices::item.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) Per aggiungere cartelle all'elenco o rimuoverle dall'elenco, usare rispettivamente i [metodi IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) [e remove.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove)

**Avvio di un'analisi**

Il monitoraggio delle cartelle è in genere un processo in background che non deve essere chiamato in modo esplicito. Per analizzare attivamente una cartella, chiamare [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). È possibile arrestare un'analisi in corso con [il metodo IWMPFolderMonitorServices::stopScan.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan)

**Recupero dello stato di monitoraggio delle cartelle**

**IWMPFolderMonitorServices offre** funzionalità per il recupero dello stato del processo di monitoraggio delle cartelle.

L'analisi delle cartelle viene eseguita in due passaggi. Nel primo passaggio, Player analizza le cartelle denominate nell'elenco delle cartelle monitorate una alla volta e compila un elenco di file da aggiungere alla libreria. Nel secondo passaggio, passa attraverso l'elenco di file e aggiunge i file alla libreria e rimuove anche tutti gli elementi multimediali dalla libreria i cui file fisici corrispondenti sono stati eliminati dal file system.

[L'evento FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) viene usato per inviare una notifica al programma ogni volta che il lettore passa a un nuovo stato. È anche possibile recuperare lo stato corrente chiamando [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). All'avvio del primo passaggio, il valore dello stato corrente è wmpfssScanning. Durante il secondo passaggio, lo stato passa a wmpfssUpdating. Al termine del processo, lo stato cambia in wmpfssStopped.

Mentre Player esegue l'analisi delle cartelle monitorate al primo passaggio, chiamare [ \_ get scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) per controllare il numero di file analizzati. Il [metodo \_ get currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) dirà quale cartella è attualmente in fase di analisi.

Dopo l'avvio del secondo passaggio, chiamare [ \_ get addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) per controllare quanti file sono stati aggiunti alla libreria. Il [metodo \_ get updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) consente di indicare lo stato del secondo passaggio, come percentuale da 0 a 100.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Interfaccia IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




