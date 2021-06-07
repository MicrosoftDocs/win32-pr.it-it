---
description: Tutti i provider di servizi devono implementare le funzioni di telefonia di base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funzioni di telefonia di base TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524155"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="20aa7-103">Funzioni di telefonia di base TSPI</span><span class="sxs-lookup"><span data-stu-id="20aa7-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="20aa7-104">Tutti i provider di servizi devono implementare le funzioni di telefonia di base.</span><span class="sxs-lookup"><span data-stu-id="20aa7-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="20aa7-105">Di seguito è riportato un elenco di tali funzioni per categoria.</span><span class="sxs-lookup"><span data-stu-id="20aa7-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="20aa7-106">Una funzione viene identificata *come asincrona* se indica il completamento in un messaggio REPLY all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="20aa7-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="20aa7-107">Se la funzione restituisce sempre immediatamente il risultato, la funzione viene considerata *sincrona.*</span><span class="sxs-lookup"><span data-stu-id="20aa7-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="20aa7-108">Indirizzi</span><span class="sxs-lookup"><span data-stu-id="20aa7-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="20aa7-109">Risposta alle chiamate in ingresso</span><span class="sxs-lookup"><span data-stu-id="20aa7-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="20aa7-110">Funzioni di rilascio delle chiamate</span><span class="sxs-lookup"><span data-stu-id="20aa7-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="20aa7-111">Chiamare stati ed eventi</span><span class="sxs-lookup"><span data-stu-id="20aa7-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="20aa7-112">Stato e funzionalità della riga</span><span class="sxs-lookup"><span data-stu-id="20aa7-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="20aa7-113">Negoziazione della versione della riga</span><span class="sxs-lookup"><span data-stu-id="20aa7-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="20aa7-114">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="20aa7-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="20aa7-115">Apertura e chiusura di dispositivi line</span><span class="sxs-lookup"><span data-stu-id="20aa7-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="20aa7-116">Negoziazione della versione del telefono</span><span class="sxs-lookup"><span data-stu-id="20aa7-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="20aa7-117">Inizializzazione e arresto di TSP</span><span class="sxs-lookup"><span data-stu-id="20aa7-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="20aa7-118">Inizializzazione e arresto di TSP</span><span class="sxs-lookup"><span data-stu-id="20aa7-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="20aa7-119">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-119">Function</span></span>                                                         |   <span data-ttu-id="20aa7-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="20aa7-121">**Provider \_ TUISPIInstalla**</span><span class="sxs-lookup"><span data-stu-id="20aa7-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="20aa7-122">Installa un TSP.</span><span class="sxs-lookup"><span data-stu-id="20aa7-122">Installs a TSP.</span></span> <span data-ttu-id="20aa7-123">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="20aa7-124">**Provider \_ TSPIInstalla**</span><span class="sxs-lookup"><span data-stu-id="20aa7-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="20aa7-125">Installa TSP.</span><span class="sxs-lookup"><span data-stu-id="20aa7-125">Installs the TSP.</span></span> <span data-ttu-id="20aa7-126">Obsoleto con la versione 2.0.</span><span class="sxs-lookup"><span data-stu-id="20aa7-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="20aa7-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-127">Synchronous.</span></span> |
| [<span data-ttu-id="20aa7-128">**Provider \_ TSPIInit**</span><span class="sxs-lookup"><span data-stu-id="20aa7-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="20aa7-129">Inizializza TSP.</span><span class="sxs-lookup"><span data-stu-id="20aa7-129">Initializes the TSP.</span></span> <span data-ttu-id="20aa7-130">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="20aa7-131">**Provider \_ TSPIShutdown**</span><span class="sxs-lookup"><span data-stu-id="20aa7-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="20aa7-132">Arresta il provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="20aa7-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="20aa7-133">**Provider \_ TUISPIRimuovi**</span><span class="sxs-lookup"><span data-stu-id="20aa7-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="20aa7-134">Rimuove un TSP.</span><span class="sxs-lookup"><span data-stu-id="20aa7-134">Removes a TSP.</span></span> <span data-ttu-id="20aa7-135">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="20aa7-136">**Provider \_ TSPIRimuovi**</span><span class="sxs-lookup"><span data-stu-id="20aa7-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="20aa7-137">Rimuove un TSP.</span><span class="sxs-lookup"><span data-stu-id="20aa7-137">Removes a TSP.</span></span> <span data-ttu-id="20aa7-138">Obsoleto con la versione 2.0.</span><span class="sxs-lookup"><span data-stu-id="20aa7-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="20aa7-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="20aa7-140">Negoziazione della versione del telefono</span><span class="sxs-lookup"><span data-stu-id="20aa7-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="20aa7-141">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-141">Function</span></span>                                                         |   <span data-ttu-id="20aa7-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-143">**Telefono \_ TSPINegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="20aa7-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="20aa7-144">Restituisce la versione SPI più elevata con cui il provider di servizi può operare per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20aa7-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="20aa7-145">Negoziazione della versione della riga</span><span class="sxs-lookup"><span data-stu-id="20aa7-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="20aa7-146">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-146">Function</span></span>                                                         |   <span data-ttu-id="20aa7-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-148">**Riga \_ TSPINegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="20aa7-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="20aa7-149">Consente a un'applicazione di negoziare una versione TSPI da usare con un determinato dispositivo di linea.</span><span class="sxs-lookup"><span data-stu-id="20aa7-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="20aa7-150">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="20aa7-151">Stato e funzionalità della riga</span><span class="sxs-lookup"><span data-stu-id="20aa7-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="20aa7-152">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-152">Function</span></span>                                                         |   <span data-ttu-id="20aa7-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-154">**Riga \_ TSPIGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="20aa7-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="20aa7-155">Restituisce le funzionalità di un dispositivo linea specificato.</span><span class="sxs-lookup"><span data-stu-id="20aa7-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="20aa7-156">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="20aa7-157">**Riga \_ TSPIGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="20aa7-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="20aa7-158">Restituisce la configurazione di un dispositivo di flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="20aa7-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="20aa7-159">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="20aa7-160">**Riga \_ TSPIGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="20aa7-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="20aa7-161">Restituisce lo stato corrente del dispositivo open line specificato.</span><span class="sxs-lookup"><span data-stu-id="20aa7-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="20aa7-162">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="20aa7-163">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="20aa7-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="20aa7-164">Imposta la configurazione del dispositivo del flusso multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="20aa7-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="20aa7-165">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="20aa7-166">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="20aa7-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="20aa7-167">Specifica le modifiche di stato per cui l'applicazione deve ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="20aa7-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="20aa7-168">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="20aa7-169">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="20aa7-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="20aa7-170">Recupera un ID dispositivo associato alla riga aperta, all'indirizzo o alla chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="20aa7-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="20aa7-171">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="20aa7-172">**Riga \_ TSPIGetIcon**</span><span class="sxs-lookup"><span data-stu-id="20aa7-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="20aa7-173">Consente a un'applicazione di recuperare un'icona da visualizzare all'utente.</span><span class="sxs-lookup"><span data-stu-id="20aa7-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="20aa7-174">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="20aa7-175">**LineConfigDialog TUISPI \_**</span><span class="sxs-lookup"><span data-stu-id="20aa7-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="20aa7-176">Fa in modo che il provider del dispositivo linea specificato visualizza una finestra di dialogo che consente all'utente di configurare i parametri correlati al dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="20aa7-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="20aa7-177">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-177">Synchronous.</span></span> |
| [<span data-ttu-id="20aa7-178">**LINEISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="20aa7-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="20aa7-179">Visualizza una finestra di dialogo che consente all'utente di modificare le informazioni di configurazione per un dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="20aa7-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="20aa7-180">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="20aa7-181">Indirizzi</span><span class="sxs-lookup"><span data-stu-id="20aa7-181">Addresses</span></span>



|  <span data-ttu-id="20aa7-182">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-182">Function</span></span>                                                         |   <span data-ttu-id="20aa7-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-184">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="20aa7-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="20aa7-185">Restituisce le funzionalità di telefonia di un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="20aa7-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="20aa7-186">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="20aa7-187">**Riga \_ TSPIGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="20aa7-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="20aa7-188">Restituisce lo stato corrente di un indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="20aa7-188">Returns current status of a specified address.</span></span> <span data-ttu-id="20aa7-189">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="20aa7-190">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="20aa7-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="20aa7-191">Recupera il numero di identificatori di indirizzo supportati nella riga indicata.</span><span class="sxs-lookup"><span data-stu-id="20aa7-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="20aa7-192">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="20aa7-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="20aa7-193">Recupera l'ID indirizzo di un indirizzo specificato usando un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="20aa7-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="20aa7-194">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="20aa7-195">Apertura e chiusura di dispositivi line</span><span class="sxs-lookup"><span data-stu-id="20aa7-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="20aa7-196">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-196">Function</span></span>                                                         |   <span data-ttu-id="20aa7-197">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-198">**Riga \_ TSPIApri**</span><span class="sxs-lookup"><span data-stu-id="20aa7-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="20aa7-199">Apre un dispositivo linea specificato per fornire il monitoraggio e/o il controllo successivi della linea.</span><span class="sxs-lookup"><span data-stu-id="20aa7-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="20aa7-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-200">Synchronous.</span></span> |
| [<span data-ttu-id="20aa7-201">**Riga \_ TSPIChiudi**</span><span class="sxs-lookup"><span data-stu-id="20aa7-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="20aa7-202">Chiude un dispositivo di linea aperto specificato.</span><span class="sxs-lookup"><span data-stu-id="20aa7-202">Closes a specified opened line device.</span></span> <span data-ttu-id="20aa7-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="20aa7-204">Chiamare stati ed eventi</span><span class="sxs-lookup"><span data-stu-id="20aa7-204">Call States and Events</span></span>



|  <span data-ttu-id="20aa7-205">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-205">Function</span></span>                                                         |   <span data-ttu-id="20aa7-206">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-207">**Riga \_ TSPIGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="20aa7-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="20aa7-208">Restituisce informazioni fisse su una chiamata.</span><span class="sxs-lookup"><span data-stu-id="20aa7-208">Returns fixed information about a call.</span></span> <span data-ttu-id="20aa7-209">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="20aa7-210">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="20aa7-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="20aa7-211">Restituisce informazioni complete sullo stato della chiamata per la chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="20aa7-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="20aa7-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-212">Synchronous.</span></span>       |
| [<span data-ttu-id="20aa7-213">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="20aa7-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="20aa7-214">Imposta il campo specifico dell'applicazione della struttura delle informazioni di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="20aa7-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="20aa7-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="20aa7-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="20aa7-216">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="20aa7-216">Making Calls</span></span>



|  <span data-ttu-id="20aa7-217">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-217">Function</span></span>                                                         |   <span data-ttu-id="20aa7-218">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-219">**Riga \_ TSPIMakeCall**</span><span class="sxs-lookup"><span data-stu-id="20aa7-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="20aa7-220">Esegue una chiamata in uscita e restituisce un handle di chiamata.</span><span class="sxs-lookup"><span data-stu-id="20aa7-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="20aa7-221">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="20aa7-221">Asynchronous.</span></span> |
| [<span data-ttu-id="20aa7-222">**\_LineDial TSPI**</span><span class="sxs-lookup"><span data-stu-id="20aa7-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="20aa7-223">Dial (parti di uno o più) indirizzi dialable.</span><span class="sxs-lookup"><span data-stu-id="20aa7-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="20aa7-224">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="20aa7-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="20aa7-225">Risposta alle chiamate in ingresso</span><span class="sxs-lookup"><span data-stu-id="20aa7-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="20aa7-226">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-226">Function</span></span>                                                         |   <span data-ttu-id="20aa7-227">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="20aa7-228">**Riga \_ TSPIAnswer**</span><span class="sxs-lookup"><span data-stu-id="20aa7-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="20aa7-229">Risponde a una chiamata in ingresso.</span><span class="sxs-lookup"><span data-stu-id="20aa7-229">Answers an incoming call.</span></span> <span data-ttu-id="20aa7-230">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="20aa7-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="20aa7-231">Funzioni di rilascio delle chiamate</span><span class="sxs-lookup"><span data-stu-id="20aa7-231">Call Drop Functions</span></span>



|  <span data-ttu-id="20aa7-232">Funzione</span><span class="sxs-lookup"><span data-stu-id="20aa7-232">Function</span></span>                                                         |   <span data-ttu-id="20aa7-233">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20aa7-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="20aa7-234">**LineDrop \_ TSPI**</span><span class="sxs-lookup"><span data-stu-id="20aa7-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="20aa7-235">Disconnette una chiamata o abbandona un tentativo di chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="20aa7-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="20aa7-236">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="20aa7-236">Asynchronous.</span></span> |



 

 

 
