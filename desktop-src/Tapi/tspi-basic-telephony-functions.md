---
description: Tutti i provider di servizi devono implementare funzioni di telefonia di base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funzioni di telefonia Basic TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885242"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="67e97-103">Funzioni di telefonia Basic TSPI</span><span class="sxs-lookup"><span data-stu-id="67e97-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="67e97-104">Tutti i provider di servizi devono implementare funzioni di telefonia di base.</span><span class="sxs-lookup"><span data-stu-id="67e97-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="67e97-105">Di seguito è riportato un elenco di tali funzioni per categoria.</span><span class="sxs-lookup"><span data-stu-id="67e97-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="67e97-106">Una funzione viene identificata come *asincrona* se indica il completamento in un messaggio di risposta all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67e97-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="67e97-107">Se la funzione restituisce sempre il risultato immediatamente, la funzione viene considerata *sincrona*.</span><span class="sxs-lookup"><span data-stu-id="67e97-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="67e97-108">Indirizzi</span><span class="sxs-lookup"><span data-stu-id="67e97-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="67e97-109">Risposta alle chiamate in ingresso</span><span class="sxs-lookup"><span data-stu-id="67e97-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="67e97-110">Funzioni drop di chiamata</span><span class="sxs-lookup"><span data-stu-id="67e97-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="67e97-111">Stati e eventi di chiamata</span><span class="sxs-lookup"><span data-stu-id="67e97-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="67e97-112">Stato e funzionalità della linea</span><span class="sxs-lookup"><span data-stu-id="67e97-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="67e97-113">Negoziazione della versione della linea</span><span class="sxs-lookup"><span data-stu-id="67e97-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="67e97-114">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="67e97-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="67e97-115">Apertura e chiusura di dispositivi linea</span><span class="sxs-lookup"><span data-stu-id="67e97-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="67e97-116">Negoziazione della versione del telefono</span><span class="sxs-lookup"><span data-stu-id="67e97-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="67e97-117">Inizializzazione e arresto di un TSP</span><span class="sxs-lookup"><span data-stu-id="67e97-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="67e97-118">Inizializzazione e arresto di un TSP</span><span class="sxs-lookup"><span data-stu-id="67e97-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="67e97-119">**\_PROVIDERINSTALL TUISPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="67e97-120">Installa un TSP.</span><span class="sxs-lookup"><span data-stu-id="67e97-120">Installs a TSP.</span></span> <span data-ttu-id="67e97-121">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="67e97-122">**\_PROVIDERINSTALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="67e97-123">Installa il TSP.</span><span class="sxs-lookup"><span data-stu-id="67e97-123">Installs the TSP.</span></span> <span data-ttu-id="67e97-124">Obsoleto con la versione 2,0.</span><span class="sxs-lookup"><span data-stu-id="67e97-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="67e97-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-125">Synchronous.</span></span> |
| [<span data-ttu-id="67e97-126">**\_PROVIDERINIT TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="67e97-127">Inizializza il TSP.</span><span class="sxs-lookup"><span data-stu-id="67e97-127">Initializes the TSP.</span></span> <span data-ttu-id="67e97-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="67e97-129">**\_PROVIDERSHUTDOWN TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="67e97-130">Arresta il provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="67e97-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="67e97-131">**\_PROVIDERREMOVE TUISPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="67e97-132">Rimuove un TSP.</span><span class="sxs-lookup"><span data-stu-id="67e97-132">Removes a TSP.</span></span> <span data-ttu-id="67e97-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="67e97-134">**\_PROVIDERREMOVE TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="67e97-135">Rimuove un TSP.</span><span class="sxs-lookup"><span data-stu-id="67e97-135">Removes a TSP.</span></span> <span data-ttu-id="67e97-136">Obsoleto con la versione 2,0.</span><span class="sxs-lookup"><span data-stu-id="67e97-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="67e97-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="67e97-138">Negoziazione della versione del telefono</span><span class="sxs-lookup"><span data-stu-id="67e97-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-139">**\_PHONENEGOTIATETSPIVERSION TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="67e97-140">Restituisce la versione SPI più elevata con cui il provider di servizi può operare per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67e97-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="67e97-141">Negoziazione della versione della linea</span><span class="sxs-lookup"><span data-stu-id="67e97-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-142">**\_LINENEGOTIATETSPIVERSION TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="67e97-143">Consente a un'applicazione di negoziare una versione di TSPI da usare con un dispositivo a linee specificato.</span><span class="sxs-lookup"><span data-stu-id="67e97-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="67e97-144">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="67e97-145">Stato e funzionalità della linea</span><span class="sxs-lookup"><span data-stu-id="67e97-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-146">**\_LINEGETDEVCAPS TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="67e97-147">Restituisce le funzionalità di una determinata periferica di linea.</span><span class="sxs-lookup"><span data-stu-id="67e97-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="67e97-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="67e97-149">**\_LINEGETDEVCONFIG TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="67e97-150">Restituisce la configurazione di un dispositivo del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="67e97-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="67e97-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="67e97-152">**\_LINEGETLINEDEVSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="67e97-153">Restituisce lo stato corrente del dispositivo a linee aperte specificato.</span><span class="sxs-lookup"><span data-stu-id="67e97-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="67e97-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="67e97-155">**\_LINESETDEVCONFIG TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="67e97-156">Imposta la configurazione del dispositivo del flusso multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="67e97-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="67e97-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="67e97-158">**\_LINESETSTATUSMESSAGES TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="67e97-159">Specifica le modifiche dello stato per le quali l'applicazione deve ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="67e97-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="67e97-160">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="67e97-161">**\_LINEGETID TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="67e97-162">Recupera un ID dispositivo associato alla riga aperta, all'indirizzo o alla chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="67e97-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="67e97-163">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="67e97-164">**\_LINEGETICON TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="67e97-165">Consente a un'applicazione di recuperare un'icona da visualizzare all'utente.</span><span class="sxs-lookup"><span data-stu-id="67e97-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="67e97-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="67e97-167">**\_LINECONFIGDIALOG TUISPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="67e97-168">Fa in modo che il provider del dispositivo a linee specificato visualizzi una finestra di dialogo che consenta all'utente di configurare i parametri correlati al dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="67e97-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="67e97-169">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-169">Synchronous.</span></span> |
| [<span data-ttu-id="67e97-170">**\_LINECONFIGDIALOGEDIT TUISPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="67e97-171">Visualizza una finestra di dialogo che consente all'utente di modificare le informazioni di configurazione per un dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="67e97-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="67e97-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="67e97-173">Indirizzi</span><span class="sxs-lookup"><span data-stu-id="67e97-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-174">**\_LINEGETADDRESSCAPS TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="67e97-175">Restituisce le funzionalità di telefonia di un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="67e97-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="67e97-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="67e97-177">**\_LINEGETADDRESSSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="67e97-178">Restituisce lo stato corrente di un indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="67e97-178">Returns current status of a specified address.</span></span> <span data-ttu-id="67e97-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="67e97-180">**\_LINEGETNUMADDRESSIDS TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="67e97-181">Recupera il numero di identificatori di indirizzo supportati sulla riga indicata.</span><span class="sxs-lookup"><span data-stu-id="67e97-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="67e97-182">**\_LINEGETADDRESSID TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="67e97-183">Recupera l'ID di un indirizzo specificato utilizzando un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="67e97-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="67e97-184">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="67e97-185">Apertura e chiusura di dispositivi linea</span><span class="sxs-lookup"><span data-stu-id="67e97-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-186">**\_LINEOPEN TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="67e97-187">Apre un dispositivo a linee specificato per fornire il monitoraggio e/o il controllo successivo della riga.</span><span class="sxs-lookup"><span data-stu-id="67e97-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="67e97-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-188">Synchronous.</span></span> |
| [<span data-ttu-id="67e97-189">**\_LINECLOSE TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="67e97-190">Chiude un dispositivo a linee aperte specificato.</span><span class="sxs-lookup"><span data-stu-id="67e97-190">Closes a specified opened line device.</span></span> <span data-ttu-id="67e97-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="67e97-192">Stati e eventi di chiamata</span><span class="sxs-lookup"><span data-stu-id="67e97-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-193">**\_LINEGETCALLINFO TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="67e97-194">Restituisce informazioni fisse su una chiamata.</span><span class="sxs-lookup"><span data-stu-id="67e97-194">Returns fixed information about a call.</span></span> <span data-ttu-id="67e97-195">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="67e97-196">**\_LINEGETCALLSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="67e97-197">Restituisce informazioni complete sullo stato della chiamata per la chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="67e97-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="67e97-198">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-198">Synchronous.</span></span>       |
| [<span data-ttu-id="67e97-199">**\_LINESETAPPSPECIFIC TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="67e97-200">Imposta il campo specifico dell'applicazione della struttura di informazioni di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="67e97-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="67e97-201">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="67e97-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="67e97-202">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="67e97-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-203">**\_LINEMAKECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="67e97-204">Esegue una chiamata in uscita e restituisce un handle di chiamata per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="67e97-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="67e97-205">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="67e97-205">Asynchronous.</span></span> |
| [<span data-ttu-id="67e97-206">**\_LINEDIAL TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="67e97-207">Dials (parti di uno o più) indirizzi di connessione.</span><span class="sxs-lookup"><span data-stu-id="67e97-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="67e97-208">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="67e97-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="67e97-209">Risposta alle chiamate in ingresso</span><span class="sxs-lookup"><span data-stu-id="67e97-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="67e97-210">**\_LINEANSWER TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="67e97-211">Risponde a una chiamata in ingresso.</span><span class="sxs-lookup"><span data-stu-id="67e97-211">Answers an incoming call.</span></span> <span data-ttu-id="67e97-212">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="67e97-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="67e97-213">Funzioni drop di chiamata</span><span class="sxs-lookup"><span data-stu-id="67e97-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="67e97-214">**\_LINEDROP TSPI**</span><span class="sxs-lookup"><span data-stu-id="67e97-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="67e97-215">Disconnette una chiamata o abbandona un tentativo di chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="67e97-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="67e97-216">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="67e97-216">Asynchronous.</span></span> |



 

 

 
