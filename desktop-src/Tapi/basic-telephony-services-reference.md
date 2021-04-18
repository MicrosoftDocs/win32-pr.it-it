---
description: Le funzioni di telefonia di base sono elencate per categoria nelle tabelle seguenti.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Guida di riferimento ai servizi di telefonia Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309977"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="90386-103">Guida di riferimento ai servizi di telefonia Basic</span><span class="sxs-lookup"><span data-stu-id="90386-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="90386-104">Le funzioni di telefonia di base sono elencate per categoria nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="90386-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="90386-105">Una funzione viene identificata come [*asincrona*](a-tapgloss.md) se indica il completamento in un messaggio di risposta all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90386-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="90386-106">Se la funzione restituisce sempre il risultato all'applicazione immediatamente, la funzione viene considerata [*sincrona*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="90386-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="90386-107">Di seguito è riportato un raggruppamento funzionale delle funzioni di base del servizio di telefonia:</span><span class="sxs-lookup"><span data-stu-id="90386-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="90386-108">Formati di indirizzi</span><span class="sxs-lookup"><span data-stu-id="90386-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="90386-109">Indirizzi</span><span class="sxs-lookup"><span data-stu-id="90386-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="90386-110">Risposta alle chiamate in ingresso</span><span class="sxs-lookup"><span data-stu-id="90386-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="90386-111">Funzioni drop di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="90386-112">Manipolazione dell'handle di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="90386-113">Controllo dei privilegi di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="90386-114">Stati e eventi di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="90386-115">Stato e funzionalità della linea</span><span class="sxs-lookup"><span data-stu-id="90386-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="90386-116">Negoziazione della versione della linea</span><span class="sxs-lookup"><span data-stu-id="90386-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="90386-117">Informazioni località e paese/area geografica</span><span class="sxs-lookup"><span data-stu-id="90386-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="90386-118">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="90386-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="90386-119">Apertura e chiusura di dispositivi linea</span><span class="sxs-lookup"><span data-stu-id="90386-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="90386-120">Richiedi servizi destinatari</span><span class="sxs-lookup"><span data-stu-id="90386-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="90386-121">Inizializzazione e arresto di TAPI</span><span class="sxs-lookup"><span data-stu-id="90386-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="90386-122">Supporto per Toll saver</span><span class="sxs-lookup"><span data-stu-id="90386-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="90386-123">Inizializzazione e arresto di TAPI</span><span class="sxs-lookup"><span data-stu-id="90386-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="90386-124">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-124">Function</span></span>                                     | <span data-ttu-id="90386-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-126">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="90386-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="90386-127">Inizializza l'astrazione della linea TAPI per l'uso da parte dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="90386-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="90386-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-128">Synchronous.</span></span> |
| [<span data-ttu-id="90386-129">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="90386-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="90386-130">Arresta l'uso dell'astrazione di linea di TAPI nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90386-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="90386-131">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="90386-132">Negoziazione della versione della linea</span><span class="sxs-lookup"><span data-stu-id="90386-132">Line Version Negotiation</span></span>



| <span data-ttu-id="90386-133">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-133">Function</span></span>                                                   | <span data-ttu-id="90386-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="90386-135">**lineNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="90386-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="90386-136">Consente a un'applicazione di negoziare una versione TAPI da usare.</span><span class="sxs-lookup"><span data-stu-id="90386-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="90386-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="90386-138">Stato e funzionalità della linea</span><span class="sxs-lookup"><span data-stu-id="90386-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="90386-139">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-139">Function</span></span>                                               | <span data-ttu-id="90386-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-141">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="90386-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="90386-142">Restituisce le funzionalità di una determinata periferica di linea.</span><span class="sxs-lookup"><span data-stu-id="90386-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="90386-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="90386-144">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="90386-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="90386-145">Restituisce la configurazione di un dispositivo del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="90386-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="90386-146">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="90386-147">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="90386-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="90386-148">Restituisce lo stato corrente del dispositivo a linee aperte specificato.</span><span class="sxs-lookup"><span data-stu-id="90386-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="90386-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="90386-150">**lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="90386-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="90386-151">Imposta la configurazione del dispositivo del flusso multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="90386-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="90386-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="90386-153">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="90386-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="90386-154">Specifica le modifiche dello stato per le quali l'applicazione deve ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="90386-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="90386-155">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="90386-156">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="90386-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="90386-157">Restituisce le impostazioni correnti dei messaggi di stato della riga e dell'indirizzo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90386-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="90386-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="90386-159">**lineGetID**</span><span class="sxs-lookup"><span data-stu-id="90386-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="90386-160">Recupera un ID dispositivo associato alla riga aperta, all'indirizzo o alla chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="90386-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="90386-161">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="90386-162">**lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="90386-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="90386-163">Consente a un'applicazione di recuperare un'icona da visualizzare all'utente.</span><span class="sxs-lookup"><span data-stu-id="90386-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="90386-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="90386-165">**lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="90386-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="90386-166">Fa in modo che il provider del dispositivo a linee specificato visualizzi una finestra di dialogo che consenta all'utente di configurare i parametri correlati al dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="90386-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="90386-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-167">Synchronous.</span></span> |
| [<span data-ttu-id="90386-168">**lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="90386-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="90386-169">Visualizza una finestra di dialogo che consente all'utente di modificare le informazioni di configurazione per un dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="90386-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="90386-170">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="90386-171">Indirizzi</span><span class="sxs-lookup"><span data-stu-id="90386-171">Addresses</span></span>



| <span data-ttu-id="90386-172">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-172">Function</span></span>                                             | <span data-ttu-id="90386-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-174">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="90386-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="90386-175">Restituisce le funzionalità di telefonia di un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="90386-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="90386-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="90386-177">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="90386-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="90386-178">Restituisce lo stato corrente di un indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="90386-178">Returns current status of a specified address.</span></span> <span data-ttu-id="90386-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="90386-180">**lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="90386-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="90386-181">Recupera l'ID di un indirizzo specificato utilizzando un formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="90386-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="90386-182">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="90386-183">Apertura e chiusura di dispositivi linea</span><span class="sxs-lookup"><span data-stu-id="90386-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="90386-184">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-184">Function</span></span>                       | <span data-ttu-id="90386-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-186">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="90386-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="90386-187">Apre un dispositivo a linee specificato per fornire il monitoraggio e/o il controllo successivo della riga.</span><span class="sxs-lookup"><span data-stu-id="90386-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="90386-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-188">Synchronous.</span></span> |
| [<span data-ttu-id="90386-189">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="90386-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="90386-190">Chiude un dispositivo a linee aperte specificato.</span><span class="sxs-lookup"><span data-stu-id="90386-190">Closes a specified opened line device.</span></span> <span data-ttu-id="90386-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="90386-192">Formati di indirizzi</span><span class="sxs-lookup"><span data-stu-id="90386-192">Address Formats</span></span>



| <span data-ttu-id="90386-193">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-193">Function</span></span>                                                 | <span data-ttu-id="90386-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-195">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="90386-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="90386-196">Trasla tra un indirizzo in formato canonico e un indirizzo in formato di composizione.</span><span class="sxs-lookup"><span data-stu-id="90386-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="90386-197">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-197">Synchronous.</span></span> |
| [<span data-ttu-id="90386-198">**lineSetCurrentLocation**</span><span class="sxs-lookup"><span data-stu-id="90386-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="90386-199">Imposta il percorso utilizzato come contesto per la conversione degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="90386-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="90386-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="90386-201">**lineSetTollList**</span><span class="sxs-lookup"><span data-stu-id="90386-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="90386-202">Modifica la lista dei caselli.</span><span class="sxs-lookup"><span data-stu-id="90386-202">Manipulates the toll list.</span></span> <span data-ttu-id="90386-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="90386-204">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="90386-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="90386-205">Restituisce le funzionalità di traduzione degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="90386-205">Returns address translation capabilities.</span></span> <span data-ttu-id="90386-206">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="90386-207">Stati e eventi di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-207">Call States and Events</span></span>



| <span data-ttu-id="90386-208">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-208">Function</span></span>                                         | <span data-ttu-id="90386-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-210">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="90386-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="90386-211">Restituisce informazioni fisse su una chiamata.</span><span class="sxs-lookup"><span data-stu-id="90386-211">Returns fixed information about a call.</span></span> <span data-ttu-id="90386-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="90386-213">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="90386-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="90386-214">Restituisce informazioni complete sullo stato della chiamata per la chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="90386-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="90386-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-215">Synchronous.</span></span>       |
| [<span data-ttu-id="90386-216">**lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="90386-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="90386-217">Imposta il campo specifico dell'applicazione della struttura di informazioni di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="90386-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="90386-218">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="90386-219">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="90386-219">Making Calls</span></span>



| <span data-ttu-id="90386-220">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-220">Function</span></span>                             | <span data-ttu-id="90386-221">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="90386-222">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="90386-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="90386-223">Esegue una chiamata in uscita e restituisce un handle di chiamata per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="90386-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="90386-224">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="90386-224">Asynchronous.</span></span> |
| [<span data-ttu-id="90386-225">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="90386-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="90386-226">Dials (parti di uno o più) indirizzi di connessione.</span><span class="sxs-lookup"><span data-stu-id="90386-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="90386-227">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="90386-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="90386-228">Risposta alle chiamate in ingresso</span><span class="sxs-lookup"><span data-stu-id="90386-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="90386-229">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-229">Function</span></span>                         | <span data-ttu-id="90386-230">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="90386-231">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="90386-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="90386-232">Risponde a una chiamata in ingresso.</span><span class="sxs-lookup"><span data-stu-id="90386-232">Answers an incoming call.</span></span> <span data-ttu-id="90386-233">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="90386-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="90386-234">Supporto per Toll saver</span><span class="sxs-lookup"><span data-stu-id="90386-234">Toll Saver Support</span></span>



| <span data-ttu-id="90386-235">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-235">Function</span></span>                                   | <span data-ttu-id="90386-236">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-237">**lineSetNumRings**</span><span class="sxs-lookup"><span data-stu-id="90386-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="90386-238">Indica il numero di anelli dopo i quali le chiamate in ingresso devono essere soddisfatte.</span><span class="sxs-lookup"><span data-stu-id="90386-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="90386-239">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="90386-240">**lineGetNumRings**</span><span class="sxs-lookup"><span data-stu-id="90386-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="90386-241">Restituisce il numero minimo di anelli richiesti con [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span><span class="sxs-lookup"><span data-stu-id="90386-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="90386-242">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="90386-243">Controllo dei privilegi di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-243">Call Privilege Control</span></span>



| <span data-ttu-id="90386-244">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-244">Function</span></span>                                             | <span data-ttu-id="90386-245">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="90386-246">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="90386-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="90386-247">Imposta il privilegio dell'applicazione sul privilegio specificato.</span><span class="sxs-lookup"><span data-stu-id="90386-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="90386-248">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="90386-249">Funzioni drop di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-249">Call Drop Functions</span></span>



| <span data-ttu-id="90386-250">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-250">Function</span></span>                                         | <span data-ttu-id="90386-251">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="90386-252">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="90386-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="90386-253">Disconnette una chiamata o abbandona un tentativo di chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="90386-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="90386-254">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="90386-254">Asynchronous.</span></span> |
| [<span data-ttu-id="90386-255">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="90386-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="90386-256">Dealloca l'handle di chiamata specificato.</span><span class="sxs-lookup"><span data-stu-id="90386-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="90386-257">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="90386-258">Manipolazione dell'handle di chiamata</span><span class="sxs-lookup"><span data-stu-id="90386-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="90386-259">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-259">Function</span></span>                                                   | <span data-ttu-id="90386-260">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-261">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="90386-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="90386-262">Passa la proprietà della chiamata e/o modifica i privilegi di un'applicazione a una chiamata.</span><span class="sxs-lookup"><span data-stu-id="90386-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="90386-263">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="90386-264">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="90386-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="90386-265">Restituisce gli handle di chiamata per le chiamate su una riga o un indirizzo specificato per cui l'applicazione non dispone ancora di handle.</span><span class="sxs-lookup"><span data-stu-id="90386-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="90386-266">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-266">Synchronous.</span></span> |
| [<span data-ttu-id="90386-267">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="90386-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="90386-268">Restituisce un elenco di handle di chiamata che fanno parte della stessa chiamata di conferenza della chiamata specificata come parametro.</span><span class="sxs-lookup"><span data-stu-id="90386-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="90386-269">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="90386-270">Informazioni località e paese/area geografica</span><span class="sxs-lookup"><span data-stu-id="90386-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="90386-271">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-271">Function</span></span>                                           | <span data-ttu-id="90386-272">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-273">**lineTranslateDialog**</span><span class="sxs-lookup"><span data-stu-id="90386-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="90386-274">Visualizza una finestra di dialogo che consente all'utente di modificare la posizione e le informazioni sulla scheda chiamante.</span><span class="sxs-lookup"><span data-stu-id="90386-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="90386-275">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-275">Synchronous.</span></span> |
| [<span data-ttu-id="90386-276">**lineGetCountry**</span><span class="sxs-lookup"><span data-stu-id="90386-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="90386-277">Recupera le regole di composizione e altre informazioni su un determinato paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="90386-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="90386-278">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="90386-279">Richiedi servizi destinatari</span><span class="sxs-lookup"><span data-stu-id="90386-279">Request Recipient Services</span></span>

<span data-ttu-id="90386-280">Le due funzioni seguenti vengono utilizzate solo per supportare la telefonia assistita.</span><span class="sxs-lookup"><span data-stu-id="90386-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="90386-281">Funzione</span><span class="sxs-lookup"><span data-stu-id="90386-281">Function</span></span>                                                             | <span data-ttu-id="90386-282">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90386-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90386-283">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="90386-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="90386-284">Registra o Annulla la registrazione dell'applicazione come destinatario della richiesta per la modalità di richiesta specificata.</span><span class="sxs-lookup"><span data-stu-id="90386-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="90386-285">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-285">Synchronous.</span></span> |
| [<span data-ttu-id="90386-286">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="90386-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="90386-287">Ottiene la richiesta successiva dalla libreria a collegamento dinamico di telefonia.</span><span class="sxs-lookup"><span data-stu-id="90386-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="90386-288">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="90386-288">Synchronous.</span></span>                                  |



 

 

 



