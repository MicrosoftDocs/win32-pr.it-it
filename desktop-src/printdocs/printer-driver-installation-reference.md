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
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="68816-103">Riferimento per l'installazione del driver della stampante</span><span class="sxs-lookup"><span data-stu-id="68816-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="68816-104">Le funzioni in questa sezione installano e configurano i driver della stampante in un computer.</span><span class="sxs-lookup"><span data-stu-id="68816-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="68816-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="68816-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68816-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="68816-106">Function</span></span></th>
<th><span data-ttu-id="68816-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68816-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68816-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-109">La funzione <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="68816-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-111">La funzione <a href="/windows/desktop/printdocs/addport"><strong>addport</strong></a> aggiunge il nome di una porta all'elenco delle porte supportate.</span><span class="sxs-lookup"><span data-stu-id="68816-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="68816-112">La funzione <strong>addport</strong> viene esportata dal monitor di porta.</span><span class="sxs-lookup"><span data-stu-id="68816-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-114">La funzione <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> installa un driver della stampante locale o remoto e associa i file di configurazione, i dati e i driver.</span><span class="sxs-lookup"><span data-stu-id="68816-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="68816-115">Per una maggiore flessibilità nell'installazione o nell'aggiornamento dei driver della stampante, utilizzare la funzione <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> perché consente l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori di data e ora).</span><span class="sxs-lookup"><span data-stu-id="68816-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="68816-116">Non è più consigliabile installare un driver della stampante senza un pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="68816-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="68816-117">In alternativa, usare <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="68816-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-119">La funzione <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> installa un driver della stampante locale o remoto e collega i file di configurazione, i dati e i driver.</span><span class="sxs-lookup"><span data-stu-id="68816-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="68816-120">Oltre a disporre delle funzionalità di <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, dispone anche di opzioni che consentono l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori temporali dei file).</span><span class="sxs-lookup"><span data-stu-id="68816-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="68816-121">Non è più consigliabile installare un driver della stampante senza un pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="68816-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="68816-122">In alternativa, usare <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="68816-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-124">La funzione <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> installa un processore di stampa sul server specificato e aggiunge il nome del processore di stampa all'elenco dei processori di stampa supportati.</span><span class="sxs-lookup"><span data-stu-id="68816-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-126">La funzione <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> installa un provider di stampa locale e collega i file di configurazione, i dati e il provider.</span><span class="sxs-lookup"><span data-stu-id="68816-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-128">La funzione <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> segnala se è installato un driver della stampante principale con un GUID, una data e una versione specificati.</span><span class="sxs-lookup"><span data-stu-id="68816-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-130">La funzione <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> rimuove un monitor di porta aggiunto dalla funzione <a href="addmonitor.md"><strong>AddMonitor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="68816-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-132">La funzione <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> Visualizza una finestra di dialogo che consente all'utente di eliminare un nome di porta.</span><span class="sxs-lookup"><span data-stu-id="68816-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-134">La funzione <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.</span><span class="sxs-lookup"><span data-stu-id="68816-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="68816-135">Per eliminare i file associati al driver, oltre a rimuovere il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati per un server, utilizzare la funzione <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="68816-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="68816-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> Elimina un driver solo se non è in uso alcuna versione del driver per l'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="68816-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> può eliminare versioni specifiche del driver.</span><span class="sxs-lookup"><span data-stu-id="68816-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-139">La funzione <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server ed Elimina i file associati al driver.</span><span class="sxs-lookup"><span data-stu-id="68816-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="68816-140">Questa funzione può anche eliminare versioni specifiche del driver.</span><span class="sxs-lookup"><span data-stu-id="68816-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-142">Elimina un pacchetto di driver della stampante dall'archivio driver.</span><span class="sxs-lookup"><span data-stu-id="68816-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-144">La funzione <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> rimuove un processore di stampa aggiunto dalla funzione <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="68816-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-146">La funzione <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> rimuove un provider di stampa aggiunto dalla funzione <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="68816-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-148">La funzione <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> recupera informazioni sui monitoraggi di porta installati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-150">La funzione <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> enumera le porte disponibili per la stampa in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-152">La funzione <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> enumera i driver della stampante installati in un server di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-154">La funzione <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> enumera i tipi di dati supportati da un processore di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-156">La funzione <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> enumera i processori di stampa installati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-158">Recupera il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="68816-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-160">La funzione <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> recupera i dati del driver per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="68816-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="68816-161">Se il driver non è installato nel computer locale, <strong>GetPrinterDriver</strong> lo installa.</span><span class="sxs-lookup"><span data-stu-id="68816-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-163">La funzione <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> recupera i dati del driver per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="68816-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="68816-164">Se il driver non è installato nel computer locale, <strong>GetPrinterDriver2</strong> lo installa e visualizza qualsiasi interfaccia utente per la finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="68816-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-166">La funzione <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> Recupera il percorso della directory del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="68816-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-168">Recupera il percorso del pacchetto di driver della stampante specificato in un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="68816-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-170">La funzione <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> Recupera il percorso della directory del processore di stampa nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="68816-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68816-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-172">Installa un driver della stampante da un pacchetto driver presente nell'archivio driver del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="68816-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68816-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="68816-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="68816-174">Carica un driver della stampante nell'archivio driver del server di stampa, in modo che possa essere installato chiamando <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="68816-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

