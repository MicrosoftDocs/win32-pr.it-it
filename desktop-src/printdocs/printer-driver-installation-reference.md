---
description: Le funzioni in questa sezione installano e configurano i driver della stampante in un computer.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Riferimento per l'installazione del driver della stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314006"
---
# <a name="printer-driver-installation-reference"></a>Riferimento per l'installazione del driver della stampante

Le funzioni in questa sezione installano e configurano i driver della stampante in un computer.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="addmonitor.md"><strong>AddMonitor</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.<br/></td>
</tr>
<tr class="even">
<td><a href="addport.md"><strong>AddPort</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/addport"><strong>addport</strong></a> aggiunge il nome di una porta all'elenco delle porte supportate. La funzione <strong>addport</strong> viene esportata dal monitor di porta.<br/></td>
</tr>
<tr class="odd">
<td><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> installa un driver della stampante locale o remoto e associa i file di configurazione, i dati e i driver.<br/> Per una maggiore flessibilità nell'installazione o nell'aggiornamento dei driver della stampante, utilizzare la funzione <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> perché consente l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori di data e ora).<br/>
<blockquote>
[!Note]<br />
Non è più consigliabile installare un driver della stampante senza un pacchetto driver. In alternativa, usare <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> installa un driver della stampante locale o remoto e collega i file di configurazione, i dati e i driver. Oltre a disporre delle funzionalità di <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, dispone anche di opzioni che consentono l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori temporali dei file).<br/>
<blockquote>
[!Note]<br />
Non è più consigliabile installare un driver della stampante senza un pacchetto driver. In alternativa, usare <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> installa un processore di stampa sul server specificato e aggiunge il nome del processore di stampa all'elenco dei processori di stampa supportati.<br/></td>
</tr>
<tr class="even">
<td><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> installa un provider di stampa locale e collega i file di configurazione, i dati e il provider.<br/></td>
</tr>
<tr class="odd">
<td><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> segnala se è installato un driver della stampante principale con un GUID, una data e una versione specificati.<br/></td>
</tr>
<tr class="even">
<td><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> rimuove un monitor di porta aggiunto dalla funzione <a href="addmonitor.md"><strong>AddMonitor</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteport.md"><strong>DeletePort</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> Visualizza una finestra di dialogo che consente all'utente di eliminare un nome di porta.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.<br/> Per eliminare i file associati al driver, oltre a rimuovere il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati per un server, utilizzare la funzione <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .<br/> <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> Elimina un driver solo se non è in uso alcuna versione del driver per l'ambiente specificato. <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> può eliminare versioni specifiche del driver.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server ed Elimina i file associati al driver. Questa funzione può anche eliminare versioni specifiche del driver.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a><br/></td>
<td>Elimina un pacchetto di driver della stampante dall'archivio driver.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> rimuove un processore di stampa aggiunto dalla funzione <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> rimuove un provider di stampa aggiunto dalla funzione <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="enummonitors.md"><strong>EnumMonitors</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> recupera informazioni sui monitoraggi di porta installati nel server specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="enumports.md"><strong>EnumPorts</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> enumera le porte disponibili per la stampa in un server specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> enumera i driver della stampante installati in un server di stampa specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> enumera i tipi di dati supportati da un processore di stampa specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> enumera i processori di stampa installati nel server specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a><br/></td>
<td>Recupera il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, <strong>GetPrinterDriver</strong> lo installa.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br/></td>
<td>La funzione <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, <strong>GetPrinterDriver2</strong> lo installa e visualizza qualsiasi interfaccia utente per la finestra specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> Recupera il percorso della directory del driver della stampante.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br/></td>
<td>Recupera il percorso del pacchetto di driver della stampante specificato in un server di stampa.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> Recupera il percorso della directory del processore di stampa nel server specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a><br/></td>
<td>Installa un driver della stampante da un pacchetto driver presente nell'archivio driver del server di stampa.<br/></td>
</tr>
<tr class="odd">
<td><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a><br/></td>
<td>Carica un driver della stampante nell'archivio driver del server di stampa, in modo che possa essere installato chiamando <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

