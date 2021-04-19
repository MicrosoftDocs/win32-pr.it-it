---
description: Le funzioni del servizio telefonico supplementare sono elencate per categoria negli argomenti seguenti.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funzioni del servizio telefonico supplementare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311868"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="da31d-103">Funzioni del servizio telefonico supplementare</span><span class="sxs-lookup"><span data-stu-id="da31d-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="da31d-104">Le funzioni del servizio telefonico supplementare sono elencate per categoria negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="da31d-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="da31d-105">Una funzione viene identificata come [*asincrona*](a-tapgloss.md) se indicherà il completamento di un messaggio di risposta all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="da31d-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="da31d-106">Se la funzione restituisce sempre il risultato all'applicazione immediatamente, la funzione viene considerata [*sincrona*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="da31d-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="da31d-107">Di seguito è riportato un raggruppamento funzionale delle funzioni del servizio telefonico supplementare:</span><span class="sxs-lookup"><span data-stu-id="da31d-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="da31d-108">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="da31d-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="da31d-109">Aree dati</span><span class="sxs-lookup"><span data-stu-id="da31d-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="da31d-110">Schermo</span><span class="sxs-lookup"><span data-stu-id="da31d-110">Display</span></span>](#display)
-   [<span data-ttu-id="da31d-111">Dispositivi hookswitch</span><span class="sxs-lookup"><span data-stu-id="da31d-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="da31d-112">Lampade</span><span class="sxs-lookup"><span data-stu-id="da31d-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="da31d-113">Apertura e chiusura di dispositivi telefonici</span><span class="sxs-lookup"><span data-stu-id="da31d-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="da31d-114">Inizializzazione e arresto del telefono</span><span class="sxs-lookup"><span data-stu-id="da31d-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="da31d-115">Funzionalità e stato del telefono</span><span class="sxs-lookup"><span data-stu-id="da31d-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="da31d-116">Negoziazione della versione del telefono</span><span class="sxs-lookup"><span data-stu-id="da31d-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="da31d-117">Anello</span><span class="sxs-lookup"><span data-stu-id="da31d-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="da31d-118">Status</span><span class="sxs-lookup"><span data-stu-id="da31d-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="da31d-119">Inizializzazione e arresto del telefono</span><span class="sxs-lookup"><span data-stu-id="da31d-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="da31d-120">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-120">Function</span></span>                                       | <span data-ttu-id="da31d-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-122">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="da31d-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="da31d-123">Inizializza l'astrazione del telefono TAPI per l'uso da parte dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="da31d-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="da31d-124">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-124">Synchronous.</span></span> |
| [<span data-ttu-id="da31d-125">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="da31d-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="da31d-126">Arresta l'uso dell'astrazione telefonica di TAPI da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="da31d-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="da31d-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="da31d-128">Negoziazione della versione del telefono</span><span class="sxs-lookup"><span data-stu-id="da31d-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="da31d-129">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-129">Function</span></span>                                                     | <span data-ttu-id="da31d-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-131">**phoneNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="da31d-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="da31d-132">Consente a un'applicazione di negoziare una versione TAPI da usare.</span><span class="sxs-lookup"><span data-stu-id="da31d-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="da31d-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="da31d-134">Apertura e chiusura di dispositivi telefonici</span><span class="sxs-lookup"><span data-stu-id="da31d-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="da31d-135">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-135">Function</span></span>                         | <span data-ttu-id="da31d-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-137">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="da31d-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="da31d-138">Apre il dispositivo telefonico specificato, assegnando all'applicazione i privilegi di proprietario o di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="da31d-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="da31d-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-139">Synchronous.</span></span> |
| [<span data-ttu-id="da31d-140">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="da31d-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="da31d-141">Chiude un dispositivo telefonico aperto specificato.</span><span class="sxs-lookup"><span data-stu-id="da31d-141">Closes a specified open phone device.</span></span> <span data-ttu-id="da31d-142">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="da31d-143">Funzionalità e stato del telefono</span><span class="sxs-lookup"><span data-stu-id="da31d-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="da31d-144">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-144">Function</span></span>                                       | <span data-ttu-id="da31d-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-146">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="da31d-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="da31d-147">Restituisce le funzionalità di un determinato dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="da31d-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="da31d-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="da31d-149">**phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="da31d-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="da31d-150">Restituisce un ID dispositivo per la classe di dispositivo specificata associata al dispositivo telefonico specificato.</span><span class="sxs-lookup"><span data-stu-id="da31d-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="da31d-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="da31d-152">**phoneGetIcon**</span><span class="sxs-lookup"><span data-stu-id="da31d-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="da31d-153">Consente a un'applicazione di recuperare un'icona da visualizzare all'utente.</span><span class="sxs-lookup"><span data-stu-id="da31d-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="da31d-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="da31d-155">**phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="da31d-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="da31d-156">Fa in modo che il provider del dispositivo telefonico specificato visualizzi una finestra di dialogo che consenta all'utente di configurare i parametri relativi al dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="da31d-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="da31d-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="da31d-158">Dispositivi hookswitch</span><span class="sxs-lookup"><span data-stu-id="da31d-158">Hookswitch Devices</span></span>



| <span data-ttu-id="da31d-159">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-159">Function</span></span>                                         | <span data-ttu-id="da31d-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-161">**phoneSetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="da31d-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="da31d-162">Imposta lo stato di hook dei dispositivi hookswitch del telefono aperto su una modalità specificata.</span><span class="sxs-lookup"><span data-stu-id="da31d-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="da31d-163">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="da31d-164">**phoneGetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="da31d-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="da31d-165">Esegue una query sulla modalità hookswitch di un dispositivo hookswitch di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="da31d-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-166">Synchronous.</span></span>          |
| [<span data-ttu-id="da31d-167">**phoneSetVolume**</span><span class="sxs-lookup"><span data-stu-id="da31d-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="da31d-168">Imposta il volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="da31d-169">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="da31d-170">**phoneGetVolume**</span><span class="sxs-lookup"><span data-stu-id="da31d-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="da31d-171">Restituisce l'impostazione del volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="da31d-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-172">Synchronous.</span></span> |
| [<span data-ttu-id="da31d-173">**phoneSetGain**</span><span class="sxs-lookup"><span data-stu-id="da31d-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="da31d-174">Imposta il guadagno del MIC di un dispositivo hookswitch di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="da31d-175">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="da31d-176">**phoneGetGain**</span><span class="sxs-lookup"><span data-stu-id="da31d-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="da31d-177">Restituisce l'impostazione di guadagno del MIC di un dispositivo hookswitch di un telefono aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="da31d-178">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="da31d-179">Visualizza</span><span class="sxs-lookup"><span data-stu-id="da31d-179">Display</span></span>



| <span data-ttu-id="da31d-180">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-180">Function</span></span>                                   | <span data-ttu-id="da31d-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-182">**phoneSetDisplay**</span><span class="sxs-lookup"><span data-stu-id="da31d-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="da31d-183">Scrive le informazioni nella visualizzazione di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="da31d-184">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-184">Asynchronous.</span></span> |
| [<span data-ttu-id="da31d-185">**phoneGetDisplay**</span><span class="sxs-lookup"><span data-stu-id="da31d-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="da31d-186">Restituisce il contenuto corrente della visualizzazione di un telefono.</span><span class="sxs-lookup"><span data-stu-id="da31d-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="da31d-187">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="da31d-188">Anello</span><span class="sxs-lookup"><span data-stu-id="da31d-188">Ring</span></span>



| <span data-ttu-id="da31d-189">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-189">Function</span></span>                             | <span data-ttu-id="da31d-190">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-191">**phoneSetRing**</span><span class="sxs-lookup"><span data-stu-id="da31d-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="da31d-192">Squilla un dispositivo telefonico aperto in base a una modalità anello specificata.</span><span class="sxs-lookup"><span data-stu-id="da31d-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="da31d-193">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-193">Asynchronous.</span></span> |
| [<span data-ttu-id="da31d-194">**phoneGetRing**</span><span class="sxs-lookup"><span data-stu-id="da31d-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="da31d-195">Restituisce la modalità corrente della suoneria di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="da31d-196">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="da31d-197">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="da31d-197">Buttons</span></span>



| <span data-ttu-id="da31d-198">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-198">Function</span></span>                                         | <span data-ttu-id="da31d-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-200">**phoneSetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="da31d-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="da31d-201">Imposta le informazioni associate a un pulsante in un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="da31d-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="da31d-202">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-202">Asynchronous.</span></span> |
| [<span data-ttu-id="da31d-203">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="da31d-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="da31d-204">Restituisce le informazioni associate a un pulsante in un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="da31d-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="da31d-205">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="da31d-206">Lampade</span><span class="sxs-lookup"><span data-stu-id="da31d-206">Lamps</span></span>



| <span data-ttu-id="da31d-207">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-207">Function</span></span>                             | <span data-ttu-id="da31d-208">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-209">**phoneSetLamp**</span><span class="sxs-lookup"><span data-stu-id="da31d-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="da31d-210">Illumina una lampada su un dispositivo telefonico aperto specificato in una determinata modalità di illuminazione lamp.</span><span class="sxs-lookup"><span data-stu-id="da31d-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="da31d-211">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-211">Asynchronous.</span></span> |
| [<span data-ttu-id="da31d-212">**phoneGetLamp**</span><span class="sxs-lookup"><span data-stu-id="da31d-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="da31d-213">Restituisce la modalità lampada corrente della lampada specificata.</span><span class="sxs-lookup"><span data-stu-id="da31d-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="da31d-214">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="da31d-215">Aree dati</span><span class="sxs-lookup"><span data-stu-id="da31d-215">Data Areas</span></span>



| <span data-ttu-id="da31d-216">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-216">Function</span></span>                             | <span data-ttu-id="da31d-217">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-218">**phoneSetData**</span><span class="sxs-lookup"><span data-stu-id="da31d-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="da31d-219">Scarica un buffer di dati in un'area dati specificata nel dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="da31d-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="da31d-220">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="da31d-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="da31d-221">**phoneGetData**</span><span class="sxs-lookup"><span data-stu-id="da31d-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="da31d-222">Carica il contenuto di una determinata area dati del dispositivo telefonico in un buffer.</span><span class="sxs-lookup"><span data-stu-id="da31d-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="da31d-223">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="da31d-224">Stato</span><span class="sxs-lookup"><span data-stu-id="da31d-224">Status</span></span>



| <span data-ttu-id="da31d-225">Funzione</span><span class="sxs-lookup"><span data-stu-id="da31d-225">Function</span></span>                                                 | <span data-ttu-id="da31d-226">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da31d-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da31d-227">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="da31d-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="da31d-228">Specifica le modifiche dello stato per cui l'applicazione vuole ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="da31d-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="da31d-229">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-229">Synchronous.</span></span> |
| [<span data-ttu-id="da31d-230">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="da31d-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="da31d-231">Restituisce le modifiche dello stato per le quali l'applicazione desidera ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="da31d-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="da31d-232">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-232">Synchronous.</span></span>   |
| [<span data-ttu-id="da31d-233">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="da31d-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="da31d-234">Restituisce lo stato completo di un dispositivo telefonico aperto.</span><span class="sxs-lookup"><span data-stu-id="da31d-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="da31d-235">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="da31d-235">Synchronous.</span></span>                         |



 

 

 



