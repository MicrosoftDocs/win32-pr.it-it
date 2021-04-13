---
title: Informazioni sul monitoraggio delle cartelle
description: Informazioni sul monitoraggio delle cartelle
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, monitoraggio cartelle
- Modello a oggetti di Windows Media Player, monitoraggio delle cartelle
- modello a oggetti, monitoraggio delle cartelle
- Controllo ActiveX Windows Media Player, monitoraggio cartelle
- Controllo ActiveX, monitoraggio cartelle
- Controllo ActiveX Windows Media Player Mobile, monitoraggio cartelle
- Windows Media Player Mobile, monitoraggio cartelle
- monitoraggio cartelle
- cartelle di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398537"
---
# <a name="about-folder-monitoring"></a>Informazioni sul monitoraggio delle cartelle

Windows Media Player può monitorare le cartelle che contengono file multimediali digitali e aggiornare la libreria quando i file vengono aggiunti o rimossi. Questa funzionalità di monitoraggio della cartella viene fornita dall'interfaccia [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .

Per utilizzare i servizi di monitoraggio delle cartelle, è necessario creare l'oggetto Player in uno stato remoto. Per ulteriori informazioni sulla comunicazione remota, vedere la pagina relativa [ai servizi remoti di Windows Media Player](remoting-the-windows-media-player-control.md). Dopo aver creato un'istanza remota del lettore, ottenere un puntatore all'interfaccia **IWMPFolderMonitorServices** chiamando **QueryInterface** sull'interfaccia [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .

Windows Media Player mantiene un elenco di cartelle monitorate. Per ottenere un elenco delle cartelle monitorate, usare i metodi [IWMPFolderMonitorServices:: Get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) e [IWMPFolderMonitorServices:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) . Per aggiungere cartelle all'elenco o rimuoverle dall'elenco, usare rispettivamente i metodi [IWMPFolderMonitorServices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) e [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) .

**Avvio di un'analisi**

Il monitoraggio delle cartelle è in genere un processo in background che non deve essere chiamato in modo esplicito. Se si desidera eseguire l'analisi attiva di una cartella, chiamare [IWMPFolderMonitorServices:: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). È possibile arrestare un'analisi in corso con il metodo [IWMPFolderMonitorServices:: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .

**Recupero dello stato di monitoraggio della cartella**

**IWMPFolderMonitorServices** fornisce funzionalità per il recupero dello stato del processo di monitoraggio della cartella.

L'analisi delle cartelle viene eseguita in due passaggi. Nel primo passaggio, il lettore analizza le cartelle denominate nell'elenco cartelle monitorate una alla volta e compila un elenco di file da aggiungere alla libreria. Nel secondo passaggio, viene eseguito l'elenco dei file e i file vengono aggiunti alla libreria e vengono rimossi anche tutti gli elementi multimediali dalla libreria i cui file fisici corrispondenti sono stati eliminati dal file system.

L'evento [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) viene usato per notificare al programma ogni volta che il giocatore passa a un nuovo stato. È anche possibile recuperare lo stato corrente chiamando [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). Quando viene avviato il primo passaggio, il valore dello stato corrente è wmpfssScanning. Durante il secondo passaggio, lo stato passa a wmpfssUpdating. Al termine del processo, lo stato passa a wmpfssStopped.

Mentre il lettore esegue l'analisi delle cartelle monitorate al primo passaggio, chiamare [get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) per verificare il numero di file analizzati. Il metodo [get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) indica la cartella attualmente sottoposta a scansione.

Una volta avviato il secondo passaggio, chiamare [get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) per verificare il numero di file aggiunti alla libreria. Il metodo [get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) indica lo stato del secondo passaggio, come percentuale da 0 a 100.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Interfaccia IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




