---
title: Errors
description: In questa sezione vengono illustrati gli errori che possono essere causati dalle funzioni dei servizi Web Windows in seguito a un errore di esecuzione del comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Errori dei servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855698"
---
# <a name="errors"></a><span data-ttu-id="0e7f3-106">Errors</span><span class="sxs-lookup"><span data-stu-id="0e7f3-106">Errors</span></span>

<span data-ttu-id="0e7f3-107">In questa sezione vengono illustrati gli errori che possono essere causati dalle funzioni dei servizi Web Windows in seguito a un errore di esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-107">This section outlines error that may be issues by Windows Web Services functions in result of a failure to execute the command.</span></span>

-   [<span data-ttu-id="0e7f3-108">Parametri out</span><span class="sxs-lookup"><span data-stu-id="0e7f3-108">Out Parameters</span></span>](#out-parameters)
-   [<span data-ttu-id="0e7f3-109">Codici errore</span><span class="sxs-lookup"><span data-stu-id="0e7f3-109">Error Codes</span></span>](#error-codes)
-   [<span data-ttu-id="0e7f3-110">Errori avanzati</span><span class="sxs-lookup"><span data-stu-id="0e7f3-110">Rich Errors</span></span>](#rich-errors)
-   [<span data-ttu-id="0e7f3-111">Errori ed errori</span><span class="sxs-lookup"><span data-stu-id="0e7f3-111">Faults and Errors</span></span>](#faults-and-errors)
-   [<span data-ttu-id="0e7f3-112">Informazioni sull'errore sensibile alla lingua</span><span class="sxs-lookup"><span data-stu-id="0e7f3-112">Language Sensitive Error Information</span></span>](#language-sensitive-error-information)
-   [<span data-ttu-id="0e7f3-113">Codici di errore canonici</span><span class="sxs-lookup"><span data-stu-id="0e7f3-113">Canonical Error Codes</span></span>](#canonical-error-codes)
-   [<span data-ttu-id="0e7f3-114">Utilizzo API non valido</span><span class="sxs-lookup"><span data-stu-id="0e7f3-114">Invalid API Usage</span></span>](#invalid-api-usage)
-   [<span data-ttu-id="0e7f3-115">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="0e7f3-115">Security</span></span>](#security)

## <a name="out-parameters"></a><span data-ttu-id="0e7f3-116">Parametri out</span><span class="sxs-lookup"><span data-stu-id="0e7f3-116">Out Parameters</span></span>

<span data-ttu-id="0e7f3-117">Come regola generale, il valore dei parametri out non viene modificato se una funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-117">As a general rule, the value of out parameters are not modified if a function fails.</span></span>

<span data-ttu-id="0e7f3-118">Se la funzione ha esito negativo, esistono alcune istanze in cui i parametri out vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-118">There are a few instances where out parameters are modified if the function fails.</span></span> <span data-ttu-id="0e7f3-119">Questi casi vengono indicati in modo esplicito nella documentazione per ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-119">These cases are explicitly called out in the documentation for each parameter.</span></span> <span data-ttu-id="0e7f3-120">Se la documentazione non menziona alcuna modifica dei parametri in caso di errore, è possibile presupporre che la funzione non le modificherà.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-120">If the documentation does not mention anything about modifying out parameters in the case of failure, then you can safely assume that the function will not modify them.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e7f3-121">Codici errore</span><span class="sxs-lookup"><span data-stu-id="0e7f3-121">Error Codes</span></span>

<span data-ttu-id="0e7f3-122">Tutti i codici di errore restituiti sono HRESULT.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-122">All error return codes are HRESULTs.</span></span> <span data-ttu-id="0e7f3-123">Questa API definisce un set di HRESULT nell' \_ intervallo Servizi WEBservices, ma restituisce anche gli errori definiti altrove nell'API Windows.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-123">This API defines a set of HRESULTs in the FACILITY\_WEBSERVICES range, but also returns errors defined elsewhere in the Windows API.</span></span>

<span data-ttu-id="0e7f3-124">Per informazioni sui codici di errore restituiti, vedere la documentazione per le API specifiche.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-124">Refer to the documentation for specific API's to learn about which error codes are returned.</span></span> <span data-ttu-id="0e7f3-125">L'elenco non deve essere esaustivo per ogni API, bensì un elenco di codici di errore per i quali sono disponibili scenari comuni per la gestione esplicita.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-125">The list is not intended to be exhaustive for each API, but rather a list of error codes for which there are common scenarios for explicit handling.</span></span> <span data-ttu-id="0e7f3-126">Un chiamante deve sempre presupporre che siano possibili altri codici di errore da qualsiasi API.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-126">A caller should always assume other error codes are possible from any API.</span></span>

<span data-ttu-id="0e7f3-127">Questa API definisce un numero relativamente ridotto di codici di errore, che corrispondono a scenari in cui un programma desidera eseguire un'azione in base all'errore.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-127">This API defines a relatively small number of error codes, which correspond to scenarios where a program will want to take action based on the error.</span></span> <span data-ttu-id="0e7f3-128">Solo i codici di errore potrebbero non essere sufficienti per determinare la causa dell'errore o per fornire una descrizione corretta del problema all'utente.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-128">Error codes alone may not be sufficient in order to determine what went wrong, or in order to provide a good description of the problem to the user.</span></span> <span data-ttu-id="0e7f3-129">La migliore comprensione del problema deriva dall'utilizzo di errori avanzati, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-129">The best understanding of the problem comes from using Rich Errors, as described below.</span></span>

## <a name="rich-errors"></a><span data-ttu-id="0e7f3-130">Errori avanzati</span><span class="sxs-lookup"><span data-stu-id="0e7f3-130">Rich Errors</span></span>

<span data-ttu-id="0e7f3-131">In aggiunta alla restituzione di un codice di errore, un chiamante può facoltativamente richiedere informazioni dettagliate sugli errori per qualsiasi chiamata API passando un oggetto [ \_ errore WS](ws-error.md) non **null**.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-131">In additional to returning an error code, a caller may optionally request rich error information for any API call by passing a non-**NULL**[WS\_ERROR](ws-error.md) object.</span></span> <span data-ttu-id="0e7f3-132">Per creare un oggetto Error, usare [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-132">To create an error object, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span></span> <span data-ttu-id="0e7f3-133">Se si verifica un errore, l'API che ha causato l'errore compilerà l'oggetto errore con contesto aggiuntivo sulla situazione di errore.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-133">If there is an error, then the API that caused the error will fill the error object with additional context about the error situation.</span></span> <span data-ttu-id="0e7f3-134">Se non è presente alcun errore, l'oggetto errore non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-134">If there is no error, then the error object is unmodified.</span></span> <span data-ttu-id="0e7f3-135">Il passaggio di un oggetto Error **null** indica che il chiamante non è interessato a informazioni dettagliate sugli errori.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-135">Passing a **NULL** error object indicates that the caller is not interested in rich error information.</span></span> <span data-ttu-id="0e7f3-136">È necessario preparare i chiamanti (compresi i callback) per gestire gli oggetti di errore **null** .</span><span class="sxs-lookup"><span data-stu-id="0e7f3-136">Callees (including callbacks) must be prepared to handle **NULL** error objects.</span></span>

<span data-ttu-id="0e7f3-137">Si noti che lo stesso oggetto Error può essere usato per più chiamate API, ma può essere usato solo per una chiamata API alla volta (in quanto è a thread singolo).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-137">Note that the same error object can be used for multiple API calls, but may only be used for one API call at a time (as it is single threaded).</span></span> <span data-ttu-id="0e7f3-138">Ogni volta che si verifica un errore, le informazioni sull'errore vengono accodate all'oggetto Error.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-138">Each time an error occurs, error information is appended to the error object.</span></span> <span data-ttu-id="0e7f3-139">Quando una catena di chiamate viene ricaricata, più funzioni possono aggiungere informazioni all'oggetto errore per fornire un contesto aggiuntivo sull'errore.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-139">As a call chain unwinds, multiple functions may add information to the error object to provide additional context about the error.</span></span> <span data-ttu-id="0e7f3-140">Per cancellare il contenuto dell'oggetto Error prima di riutilizzarlo (dopo che si è verificato un errore), utilizzare [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-140">To clear the contents of the error object before reusing it (after an error occurs), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span></span> <span data-ttu-id="0e7f3-141">Se non si verificano errori, non è necessario reimpostare l'oggetto errore prima di riutilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-141">If no error occurs, it is not necessary to reset the error object before reusing it.</span></span>

<span data-ttu-id="0e7f3-142">Le informazioni dettagliate sugli errori sono costituite dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-142">Rich error information consists of the following:</span></span>

-   <span data-ttu-id="0e7f3-143">Set di valori di proprietà che fornisce informazioni aggiuntive sull'errore, se presente.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-143">A set of property values, which provide additional information about the error if present.</span></span> <span data-ttu-id="0e7f3-144">Vedere [**\_ \_ Proprietà WS Error**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-144">See [**WS\_ERROR\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span></span>
-   <span data-ttu-id="0e7f3-145">Zero o più stringhe di errore.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-145">Zero or more error strings.</span></span> <span data-ttu-id="0e7f3-146">Le stringhe vengono aggiunte utilizzando [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)e possono essere sottoposte a query utilizzando [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-146">The strings are added using [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring), and can be queried using using [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span></span> <span data-ttu-id="0e7f3-147">Il numero di stringhe può essere sottoposto a query utilizzando il [**\_ conteggio delle stringhe di \_ proprietà \_ \_ WS Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-147">The number of strings can be queried using [**WS\_ERROR\_PROPERTY\_STRING\_COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="faults-and-errors"></a><span data-ttu-id="0e7f3-148">Errori ed errori</span><span class="sxs-lookup"><span data-stu-id="0e7f3-148">Faults and Errors</span></span>

<span data-ttu-id="0e7f3-149">Vedere [errori](faults.md) per informazioni sul modo in cui sono correlati gli errori e gli errori.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-149">See [Faults](faults.md) for information about how errors and faults relate.</span></span>

## <a name="language-sensitive-error-information"></a><span data-ttu-id="0e7f3-150">Informazioni sull'errore sensibile alla lingua</span><span class="sxs-lookup"><span data-stu-id="0e7f3-150">Language Sensitive Error Information</span></span>

<span data-ttu-id="0e7f3-151">Quando si crea un oggetto Error, viene specificato il LANGID della traduzione della lingua desiderata per le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-151">When creating an error object, the LANGID of the desired language translation for error information is specified.</span></span> <span data-ttu-id="0e7f3-152">Viene utilizzato quando si aggiungono informazioni sugli errori all'oggetto Error.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-152">This is used when adding error information to the error object.</span></span>

<span data-ttu-id="0e7f3-153">Questo valore di lingua può essere recuperato o impostato utilizzando la [**\_ Proprietà WS Error \_ \_ LangID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-153">This language value can be retrieved or set using [**WS\_ERROR\_PROPERTY\_LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="canonical-error-codes"></a><span data-ttu-id="0e7f3-154">Codici di errore canonici</span><span class="sxs-lookup"><span data-stu-id="0e7f3-154">Canonical Error Codes</span></span>

<span data-ttu-id="0e7f3-155">Questa API fornisce un set di codici di errore (WS \_ E \_ \* ) canonico che consente di utilizzare diverse tecnologie di comunicazione senza dover dipendere dai codici di errore specifici dell'implementazione sottostante specifica.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-155">This API provides a canonical set of error codes (WS\_E\_\*) that allow for different communication technologies to be used without having to depend on the specific error codes of the specific underlying implementation.</span></span> <span data-ttu-id="0e7f3-156">Per un elenco completo di questi codici di errore, vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0e7f3-156">For a complete list of these error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="0e7f3-157">Questo consente, ad esempio, a un programma di verificare se il codice di errore **WS \_ e \_ endpoint \_ non \_** è stato trovato se si utilizza TCP, UDP o http ed eseguire un'azione, ad esempio il tentativo di utilizzare un endpoint diverso.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-157">This allows, for example, a program to check for the error code **WS\_E\_ENDPOINT\_NOT\_FOUND** whether using TCP, UDP, or HTTP, and take some action (like attempting to use a different endpoint).</span></span>

<span data-ttu-id="0e7f3-158">Quando viene eseguito il mapping di un codice di errore specifico dell'implementazione a un errore canonico, il codice di errore originale viene salvato nell'oggetto Error ed è ancora possibile accedervi per scopi diagnostici.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-158">When an implementation specific error code is mapped to a canonical error, the original error code is saved in the error object, and may still be accessed for diagnostic purposes.</span></span> <span data-ttu-id="0e7f3-159">Per ulteriori informazioni, vedere il [**\_ \_ \_ \_ \_ codice di errore originale della proprietà WS Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) .</span><span class="sxs-lookup"><span data-stu-id="0e7f3-159">See [**WS\_ERROR\_PROPERTY\_ORIGINAL\_ERROR\_CODE**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) for more information.</span></span>

## <a name="invalid-api-usage"></a><span data-ttu-id="0e7f3-160">Utilizzo API non valido</span><span class="sxs-lookup"><span data-stu-id="0e7f3-160">Invalid API Usage</span></span>

<span data-ttu-id="0e7f3-161">I codici di errore seguenti sono riservati per l'utilizzo dell'API non valido e non verranno restituiti in altre circostanze.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-161">The following error codes are reserved for invalid API usage, and will not be returned in other circumstances.</span></span> <span data-ttu-id="0e7f3-162">Se viene restituito uno di questi errori, può essere un'indicazione di un bug dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-162">If any of these errors are returned it may be an indication of an application bug.</span></span>

-   <span data-ttu-id="0e7f3-163">**\_operazione WS E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-163">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="0e7f3-164">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-164">**E\_INVALIDARG**</span></span>

<span data-ttu-id="0e7f3-165">Le enumerazioni seguenti fanno parte della traccia:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-165">The following enumerations are part of tracing:</span></span>

-   [<span data-ttu-id="0e7f3-166">**\_ \_ ID proprietà errore \_ WS**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-166">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="0e7f3-167">**\_codice eccezione \_ WS**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-167">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="0e7f3-168">I codici di errore seguenti fanno parte della traccia:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-168">The following error codes are part of tracing:</span></span>

-   <span data-ttu-id="0e7f3-169">**CERT \_ E \_ CN \_ Nessuna \_ corrispondenza**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-169">**CERT\_E\_CN\_NO\_MATCH**</span></span>
-   <span data-ttu-id="0e7f3-170">**CERTIFICATO \_ E \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-170">**CERT\_E\_EXPIRED**</span></span>
-   <span data-ttu-id="0e7f3-171">**CERTIFICATO \_ E \_ UNTRUSTEDROOT**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-171">**CERT\_E\_UNTRUSTEDROOT**</span></span>
-   <span data-ttu-id="0e7f3-172">**uso di CERT \_ E \_ errato \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-172">**CERT\_E\_WRONG\_USAGE**</span></span>
-   <span data-ttu-id="0e7f3-173">**REVOCA della crittografia \_ E in \_ \_ modalità offline**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-173">**CRYPT\_E\_REVOCATION\_OFFLINE**</span></span>
-   <span data-ttu-id="0e7f3-174">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-174">**E\_INVALIDARG**</span></span>
-   <span data-ttu-id="0e7f3-175">**E \_ OutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-175">**E\_OUTOFMEMORY**</span></span>
-   <span data-ttu-id="0e7f3-176">**\_Indirizzo WS \_ E \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-176">**WS\_E\_ADDRESS\_IN\_USE**</span></span>
-   <span data-ttu-id="0e7f3-177">**\_Indirizzo WS \_ E \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-177">**WS\_E\_ADDRESS\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="0e7f3-178">**\_ \_ accesso all'endpoint WS E \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-178">**WS\_E\_ENDPOINT\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="0e7f3-179">**\_ \_ azione endpoint WS \_ E \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-179">**WS\_E\_ENDPOINT\_ACTION\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="0e7f3-180">**WS \_ E \_ endpoint \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-180">**WS\_E\_ENDPOINT\_DISCONNECTED**</span></span>
-   <span data-ttu-id="0e7f3-181">**\_ \_ errore endpoint WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-181">**WS\_E\_ENDPOINT\_FAILURE**</span></span>
-   <span data-ttu-id="0e7f3-182">**\_ \_ errore endpoint WS \_ E \_ ricevuto**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-182">**WS\_E\_ENDPOINT\_FAULT\_RECEIVED**</span></span>
-   <span data-ttu-id="0e7f3-183">**\_endpoint WS \_ E \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-183">**WS\_E\_ENDPOINT\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="0e7f3-184">**\_endpoint WS \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-184">**WS\_E\_ENDPOINT\_NOT\_FOUND**</span></span>
-   <span data-ttu-id="0e7f3-185">**WS \_ E \_ endpoint \_ troppo \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-185">**WS\_E\_ENDPOINT\_TOO\_BUSY**</span></span>
-   <span data-ttu-id="0e7f3-186">**\_endpoint WS E non \_ \_ raggiungibile**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-186">**WS\_E\_ENDPOINT\_UNREACHABLE**</span></span>
-   <span data-ttu-id="0e7f3-187">**\_URL endpoint WS E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-187">**WS\_E\_INVALID\_ENDPOINT\_URL**</span></span>
-   <span data-ttu-id="0e7f3-188">**\_formato WS E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-188">**WS\_E\_INVALID\_FORMAT**</span></span>
-   <span data-ttu-id="0e7f3-189">**\_operazione WS E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-189">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="0e7f3-190">**WS \_ E \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-190">**WS\_E\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="0e7f3-191">**WS \_ E \_ Nessuna \_ conversione \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-191">**WS\_E\_NO\_TRANSLATION\_AVAILABLE**</span></span>
-   <span data-ttu-id="0e7f3-192">**\_ \_ overflow numerico WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-192">**WS\_E\_NUMERIC\_OVERFLOW**</span></span>
-   <span data-ttu-id="0e7f3-193">**errore di WS \_ E \_ Object \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-193">**WS\_E\_OBJECT\_FAULTED**</span></span>
-   <span data-ttu-id="0e7f3-194">**\_operazione WS \_ E \_ abbandonata**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-194">**WS\_E\_OPERATION\_ABANDONED**</span></span>
-   <span data-ttu-id="0e7f3-195">**\_operazione WS \_ E \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-195">**WS\_E\_OPERATION\_ABORTED**</span></span>
-   <span data-ttu-id="0e7f3-196">**\_timeout dell' \_ operazione WS E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-196">**WS\_E\_OPERATION\_TIMED\_OUT**</span></span>
-   <span data-ttu-id="0e7f3-197">**WS \_ E \_ altro**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-197">**WS\_E\_OTHER**</span></span>
-   <span data-ttu-id="0e7f3-198">**\_ \_ accesso proxy WS \_ E \_ negato**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-198">**WS\_E\_PROXY\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="0e7f3-199">**\_ \_ errore proxy WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-199">**WS\_E\_PROXY\_FAILURE**</span></span>
-   <span data-ttu-id="0e7f3-200">**WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione di base**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-200">**WS\_E\_PROXY\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-201">**WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione digest**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-201">**WS\_E\_PROXY\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-202">**WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione Negotiate**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-202">**WS\_E\_PROXY\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-203">**WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione NTLM**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-203">**WS\_E\_PROXY\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-204">**\_quota WS \_ E \_ superata**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-204">**WS\_E\_QUOTA\_EXCEEDED**</span></span>
-   <span data-ttu-id="0e7f3-205">**\_errore del \_ sistema di protezione WS E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-205">**WS\_E\_SECURITY\_SYSTEM\_FAILURE**</span></span>
-   <span data-ttu-id="0e7f3-206">**\_token di \_ sicurezza WS E \_ \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-206">**WS\_E\_SECURITY\_TOKEN\_EXPIRED**</span></span>
-   <span data-ttu-id="0e7f3-207">**\_errore di \_ Verifica di sicurezza WS E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-207">**WS\_E\_SECURITY\_VERIFICATION\_FAILURE**</span></span>
-   <span data-ttu-id="0e7f3-208">**WS \_ E \_ server \_ richiede \_ l' \_ autenticazione di base**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-208">**WS\_E\_SERVER\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-209">**WS \_ E \_ server \_ richiede \_ l' \_ autenticazione digest**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-209">**WS\_E\_SERVER\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-210">**WS \_ E \_ server \_ richiede \_ l' \_ autenticazione Negotiate**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-210">**WS\_E\_SERVER\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-211">**WS \_ E \_ server \_ richiede \_ l' \_ autenticazione NTLM**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-211">**WS\_E\_SERVER\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="0e7f3-212">**WS \_ S \_ asincrono**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-212">**WS\_S\_ASYNC**</span></span>
-   <span data-ttu-id="0e7f3-213">**\_fine WS \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-213">**WS\_S\_END**</span></span>

<span data-ttu-id="0e7f3-214">Le funzioni seguenti fanno parte della traccia:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-214">The following functions are part of tracing:</span></span>

-   [<span data-ttu-id="0e7f3-215">**\_ \_ ID proprietà errore \_ WS**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-215">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="0e7f3-216">**\_codice eccezione \_ WS**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-216">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="0e7f3-217">Il seguente handle fa parte della traccia:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-217">The following handle is part of tracing:</span></span>

-   [<span data-ttu-id="0e7f3-218">\_errore WS</span><span class="sxs-lookup"><span data-stu-id="0e7f3-218">WS\_ERROR</span></span>](ws-error.md)

<span data-ttu-id="0e7f3-219">La struttura seguente fa parte della traccia:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-219">The following structure is part of tracing:</span></span>

-   [<span data-ttu-id="0e7f3-220">**\_Proprietà WS Error \_**</span><span class="sxs-lookup"><span data-stu-id="0e7f3-220">**WS\_ERROR\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a><span data-ttu-id="0e7f3-221">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="0e7f3-221">Security</span></span>

<span data-ttu-id="0e7f3-222">È necessario tenere presenti alcune considerazioni di sicurezza che l'utente dell'oggetto Error deve tenere presente:</span><span class="sxs-lookup"><span data-stu-id="0e7f3-222">There are a number of security considerations that the user of the error object should be aware of:</span></span>

-   <span data-ttu-id="0e7f3-223">L'oggetto Error può contenere dati non attendibili.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-223">The error object may contain untrusted data.</span></span> <span data-ttu-id="0e7f3-224">Gli esempi sono: l'errore WS \_ e le stringhe di errore, che possono essere memorizzate nell'oggetto errore in base alle informazioni ricevute su un canale non attendibile.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-224">Examples of this are: the WS\_FAULT, and the error strings, both of which can be stored in the error object based on information received over an untrusted channel.</span></span> <span data-ttu-id="0e7f3-225">Per esaminare le informazioni nell'oggetto errore e prendere decisioni in base ai relativi valori, è necessario prestare attenzione all'utente dell'oggetto Error.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-225">The user of the error object should be careful when inspecting the information in the error object and making decisions based on its values.</span></span>
-   <span data-ttu-id="0e7f3-226">Un utente dell'oggetto Error deve chiamare [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) dopo aver esaminato le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-226">A user of the error object should call [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) after inspecting the information about the error.</span></span> <span data-ttu-id="0e7f3-227">In caso contrario, può causare un accumulo di memoria.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-227">Failing to do so can lead to memory accumulation.</span></span>
-   <span data-ttu-id="0e7f3-228">Un utente dell'oggetto Error deve prestare particolare attenzione quando si usa il \_ \_ \_ valore di divulgazione di errore completo WS dell'enumerazione di [**\_ \_ divulgazione degli errori WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , perché l'errore generato potrebbe contenere informazioni private accumulate come parte del processo di registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="0e7f3-228">A user of the error object should be very careful when using the WS\_FULL\_FAULT\_DISCLOSURE value of the [**WS\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) enumeration, because the generated fault could contain private information that was accumulated as part of the error recording process.</span></span>

 

 




