---
title: Gestione di localizzatori di risorse uniformi
description: Un Uniform Resource Locator (URL) è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104566040"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="33fa8-103">Gestione di localizzatori di risorse uniformi</span><span class="sxs-lookup"><span data-stu-id="33fa8-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="33fa8-104">Un Uniform Resource Locator (URL) è una rappresentazione compatta del percorso e del metodo di accesso per una risorsa che si trova su Internet.</span><span class="sxs-lookup"><span data-stu-id="33fa8-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="33fa8-105">Ogni URL è costituito da uno schema (HTTP, HTTPS o FTP) e da una stringa specifica dello schema.</span><span class="sxs-lookup"><span data-stu-id="33fa8-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="33fa8-106">Questa stringa può includere anche una combinazione di percorso di directory, stringa di ricerca o nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="33fa8-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="33fa8-107">Le funzioni WinINet offrono la possibilità di creare, combinare, suddividere e Canonicalize URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="33fa8-108">Per ulteriori informazioni sugli URL, vedere [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) su Uniform Resource Locator (URL).</span><span class="sxs-lookup"><span data-stu-id="33fa8-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="33fa8-109">Le funzioni URL operano in modo orientato alle attività.</span><span class="sxs-lookup"><span data-stu-id="33fa8-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="33fa8-110">Il contenuto e il formato dell'URL assegnato alla funzione non vengono verificati.</span><span class="sxs-lookup"><span data-stu-id="33fa8-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="33fa8-111">L'applicazione chiamante deve tenere traccia dell'utilizzo di queste funzioni per assicurarsi che i dati siano nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="33fa8-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="33fa8-112">La funzione [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) , ad esempio, converte il carattere "%" nella sequenza di escape "%25" quando non si utilizzano flag.</span><span class="sxs-lookup"><span data-stu-id="33fa8-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="33fa8-113">Se si utilizza [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) nell'URL canonico, la sequenza di escape "%25" verrebbe convertita nella sequenza di escape "%2525", che non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="33fa8-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="33fa8-114">Che cos'è un URL in formato canonico?</span><span class="sxs-lookup"><span data-stu-id="33fa8-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="33fa8-115">Utilizzo delle funzioni WinINet per la gestione degli URL</span><span class="sxs-lookup"><span data-stu-id="33fa8-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="33fa8-116">URL forma canonica</span><span class="sxs-lookup"><span data-stu-id="33fa8-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="33fa8-117">Combinazione degli URL di base e relativi</span><span class="sxs-lookup"><span data-stu-id="33fa8-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="33fa8-118">URL di cracking</span><span class="sxs-lookup"><span data-stu-id="33fa8-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="33fa8-119">Creazione di URL</span><span class="sxs-lookup"><span data-stu-id="33fa8-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="33fa8-120">Accesso diretto agli URL</span><span class="sxs-lookup"><span data-stu-id="33fa8-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="33fa8-121">Che cos'è un URL in formato canonico?</span><span class="sxs-lookup"><span data-stu-id="33fa8-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="33fa8-122">Il formato di tutti gli URL deve seguire la sintassi e la semantica accettate per accedere alle risorse tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="33fa8-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="33fa8-123">La canonizzazione è il processo di formattazione di un URL per seguire la sintassi e la semantica accettate.</span><span class="sxs-lookup"><span data-stu-id="33fa8-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="33fa8-124">I caratteri che devono essere codificati includono qualsiasi carattere senza carattere grafico corrispondente nel set di caratteri US-ASCII codificato (esadecimale 80-FF, che non vengono usati nel set di caratteri US-ASCII codificato, ed esadecimali 00-1F e 7F, che sono caratteri di controllo), spazi vuoti, "%" (usato per codificare altri caratteri) e caratteri unsafe (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] è).</span><span class="sxs-lookup"><span data-stu-id="33fa8-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="33fa8-125">Utilizzo delle funzioni WinINet per la gestione degli URL</span><span class="sxs-lookup"><span data-stu-id="33fa8-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="33fa8-126">Nella tabella seguente sono riepilogate le funzioni URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="33fa8-127">Funzione</span><span class="sxs-lookup"><span data-stu-id="33fa8-127">Function</span></span>                                                   | <span data-ttu-id="33fa8-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33fa8-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="33fa8-129">**InternetCanonicalizeUrl**</span><span class="sxs-lookup"><span data-stu-id="33fa8-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="33fa8-130">Canonicalizes l'URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="33fa8-131">**InternetCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="33fa8-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="33fa8-132">Combina gli URL di base e relativi.</span><span class="sxs-lookup"><span data-stu-id="33fa8-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="33fa8-133">**InternetCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="33fa8-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="33fa8-134">Analizza una stringa URL in componenti.</span><span class="sxs-lookup"><span data-stu-id="33fa8-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="33fa8-135">**InternetCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="33fa8-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="33fa8-136">Crea una stringa URL da Components.</span><span class="sxs-lookup"><span data-stu-id="33fa8-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="33fa8-137">**InternetOpenUrl**</span><span class="sxs-lookup"><span data-stu-id="33fa8-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="33fa8-138">Inizia a recuperare una risorsa FTP, HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="33fa8-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="33fa8-139">URL forma canonica</span><span class="sxs-lookup"><span data-stu-id="33fa8-139">Canonicalizing URLs</span></span>

<span data-ttu-id="33fa8-140">Forma canonica un URL è il processo che converte un URL, che può contenere caratteri non sicuri, ad esempio spazi vuoti, caratteri riservati e così via, in un formato accettato.</span><span class="sxs-lookup"><span data-stu-id="33fa8-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="33fa8-141">La funzione [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) può essere usata per Canonicalize URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="33fa8-142">Questa funzione è molto orientata alle attività, quindi l'applicazione deve tenere traccia del suo utilizzo con attenzione.</span><span class="sxs-lookup"><span data-stu-id="33fa8-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="33fa8-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) non verifica che l'URL passato sia già canonico e che l'URL restituito sia valido.</span><span class="sxs-lookup"><span data-stu-id="33fa8-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="33fa8-144">I cinque flag seguenti controllano il modo in cui [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) gestisce un URL specifico.</span><span class="sxs-lookup"><span data-stu-id="33fa8-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="33fa8-145">I flag possono essere utilizzati in combinazione.</span><span class="sxs-lookup"><span data-stu-id="33fa8-145">The flags can be used in combination.</span></span> <span data-ttu-id="33fa8-146">Se non viene usato alcun flag, la funzione codifica l'URL per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33fa8-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="33fa8-147">Valore</span><span class="sxs-lookup"><span data-stu-id="33fa8-147">Value</span></span>                     | <span data-ttu-id="33fa8-148">Significato</span><span class="sxs-lookup"><span data-stu-id="33fa8-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33fa8-149">\_modalità browser \_ ICU</span><span class="sxs-lookup"><span data-stu-id="33fa8-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="33fa8-150">Non codificare o decodificare i caratteri dopo " \# " o "?" e non rimuovere gli spazi vuoti finali dopo "?".</span><span class="sxs-lookup"><span data-stu-id="33fa8-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="33fa8-151">Se questo valore non viene specificato, l'intero URL viene codificato e gli spazi vuoti finali vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="33fa8-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="33fa8-152">DECODIFICA di ICU \_</span><span class="sxs-lookup"><span data-stu-id="33fa8-152">ICU\_DECODE</span></span>               | <span data-ttu-id="33fa8-153">Converte tutte le sequenze% XX in caratteri, incluse le sequenze di escape, prima dell'analisi dell'URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="33fa8-154">\_ \_ solo spazi di codifica ICU \_</span><span class="sxs-lookup"><span data-stu-id="33fa8-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="33fa8-155">Codifica solo gli spazi.</span><span class="sxs-lookup"><span data-stu-id="33fa8-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="33fa8-156">\_non \_ codifica ICU</span><span class="sxs-lookup"><span data-stu-id="33fa8-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="33fa8-157">Non convertire i caratteri non sicuri in sequenze di escape.</span><span class="sxs-lookup"><span data-stu-id="33fa8-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="33fa8-158">ICU \_ No \_ meta</span><span class="sxs-lookup"><span data-stu-id="33fa8-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="33fa8-159">Non rimuovere le metasequenze (ad esempio "." e "..") dall'URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="33fa8-160">Il \_ flag di decodifica di ICU deve essere usato solo su URL in formato canonico, perché presuppone che tutte le sequenze% XX siano codici di escape e li converte nei caratteri indicati dal codice.</span><span class="sxs-lookup"><span data-stu-id="33fa8-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="33fa8-161">Se l'URL contiene un simbolo "%" che non fa parte di un codice di escape, il \_ DEcodificatore di ICU lo considera comunque come uno.</span><span class="sxs-lookup"><span data-stu-id="33fa8-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="33fa8-162">Questa caratteristica potrebbe causare la creazione di un URL non valido in [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) .</span><span class="sxs-lookup"><span data-stu-id="33fa8-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="33fa8-163">Per usare [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) per restituire un URL completamente decodificato, \_ è necessario specificare i flag ICU Decode e ICU \_ senza \_ codifica.</span><span class="sxs-lookup"><span data-stu-id="33fa8-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="33fa8-164">Questa installazione presuppone che l'URL passato a [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) sia stato precedentemente reso canonico.</span><span class="sxs-lookup"><span data-stu-id="33fa8-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="33fa8-165">Combinazione degli URL di base e relativi</span><span class="sxs-lookup"><span data-stu-id="33fa8-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="33fa8-166">Un URL relativo è una rappresentazione compatta della posizione di una risorsa relativa a un URL di base assoluto.</span><span class="sxs-lookup"><span data-stu-id="33fa8-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="33fa8-167">L'URL di base deve essere noto al parser e in genere include lo schema, il percorso di rete e le parti del percorso URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="33fa8-168">Un'applicazione può chiamare [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) per combinare l'URL relativo con l'URL di base.</span><span class="sxs-lookup"><span data-stu-id="33fa8-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="33fa8-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) canonicalizes anche l'URL risultante.</span><span class="sxs-lookup"><span data-stu-id="33fa8-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="33fa8-170">URL di cracking</span><span class="sxs-lookup"><span data-stu-id="33fa8-170">Cracking URLs</span></span>

<span data-ttu-id="33fa8-171">La funzione [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) separa un URL nelle relative parti componente e restituisce i componenti indicati dalla struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) passati alla funzione.</span><span class="sxs-lookup"><span data-stu-id="33fa8-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="33fa8-172">I componenti che costituiscono la struttura [**dei \_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sono il numero di schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e informazioni aggiuntive, ad esempio i parametri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="33fa8-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="33fa8-173">Ogni componente, ad eccezione dello schema e dei numeri di porta, dispone di un membro di stringa che contiene le informazioni e un membro che contiene la lunghezza del membro della stringa.</span><span class="sxs-lookup"><span data-stu-id="33fa8-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="33fa8-174">Lo schema e i numeri di porta hanno solo un membro che archivia il valore corrispondente. vengono entrambi restituiti per tutte le chiamate riuscite a [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span><span class="sxs-lookup"><span data-stu-id="33fa8-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="33fa8-175">Per ottenere il valore di un particolare componente nella struttura [**dei \_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , il membro che archivia la lunghezza di stringa di tale componente deve essere impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="33fa8-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="33fa8-176">Il membro della stringa può essere l'indirizzo di un buffer o **null**.</span><span class="sxs-lookup"><span data-stu-id="33fa8-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="33fa8-177">Se il membro del puntatore contiene l'indirizzo di un buffer, il membro della lunghezza della stringa deve contenere la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="33fa8-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="33fa8-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) restituisce le informazioni sul componente come stringa nel buffer e archivia la lunghezza della stringa nel membro della lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="33fa8-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="33fa8-179">Se il membro del puntatore è **null**, il membro della lunghezza della stringa può essere impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="33fa8-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="33fa8-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) archivia l'indirizzo del primo carattere della stringa dell'URL che contiene le informazioni sul componente e imposta la lunghezza della stringa sul numero di caratteri nella parte rimanente della stringa dell'URL relativa al componente.</span><span class="sxs-lookup"><span data-stu-id="33fa8-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="33fa8-181">Tutti i membri del puntatore impostati su **null** con un membro di lunghezza diverso da zero puntano al punto di partenza appropriato nella stringa dell'URL.</span><span class="sxs-lookup"><span data-stu-id="33fa8-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="33fa8-182">La lunghezza archiviata nel membro length deve essere utilizzata per determinare la fine delle informazioni del singolo componente.</span><span class="sxs-lookup"><span data-stu-id="33fa8-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="33fa8-183">Per completare l'inizializzazione corretta della struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , è necessario impostare il membro **dwStructSize** sulla dimensione della struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , in byte.</span><span class="sxs-lookup"><span data-stu-id="33fa8-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="33fa8-184">Nell'esempio seguente vengono restituiti i componenti dell'URL nella casella di modifica, IDC \_ PreOpen1, e i componenti vengono restituiti alla casella di riepilogo, IDC \_ preopen List.</span><span class="sxs-lookup"><span data-stu-id="33fa8-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="33fa8-185">Per visualizzare solo le informazioni per un singolo componente, questa funzione copia il carattere immediatamente dopo le informazioni del componente nella stringa e lo sostituisce temporaneamente con un **valore null**.</span><span class="sxs-lookup"><span data-stu-id="33fa8-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="33fa8-186">Creazione di URL</span><span class="sxs-lookup"><span data-stu-id="33fa8-186">Creating URLs</span></span>

<span data-ttu-id="33fa8-187">La funzione [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) usa le informazioni contenute nella struttura dei [**\_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) per creare un Uniform Resource Locator.</span><span class="sxs-lookup"><span data-stu-id="33fa8-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="33fa8-188">I componenti che costituiscono la struttura [**dei \_ componenti URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sono lo schema, il nome host, il numero di porta, il nome utente, la password, il percorso URL e informazioni aggiuntive, ad esempio i parametri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="33fa8-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="33fa8-189">Ogni componente, eccetto il numero di porta, dispone di un membro di stringa che contiene le informazioni e un membro che contiene la lunghezza del membro della stringa.</span><span class="sxs-lookup"><span data-stu-id="33fa8-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="33fa8-190">Per ogni componente richiesto, il membro del puntatore deve contenere l'indirizzo del buffer che contiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="33fa8-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="33fa8-191">Il membro length deve essere impostato su zero se il membro del puntatore contiene l'indirizzo di una stringa con terminazione zero. il membro length deve essere impostato sulla lunghezza della stringa se il membro del puntatore contiene l'indirizzo di una stringa senza terminazione zero.</span><span class="sxs-lookup"><span data-stu-id="33fa8-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="33fa8-192">Il membro del puntatore di tutti i componenti non necessari deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="33fa8-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="33fa8-193">Accesso diretto agli URL</span><span class="sxs-lookup"><span data-stu-id="33fa8-193">Accessing URLs Directly</span></span>

<span data-ttu-id="33fa8-194">È possibile accedere direttamente alle risorse FTP e HTTP su Internet usando le funzioni [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="33fa8-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="33fa8-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) apre una connessione alla risorsa in corrispondenza dell'URL passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="33fa8-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="33fa8-196">Quando si effettua questa connessione, è possibile eseguire due passaggi.</span><span class="sxs-lookup"><span data-stu-id="33fa8-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="33fa8-197">Prima di tutto, se la risorsa è un file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) può scaricarlo; in secondo luogo, se la risorsa è una directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) può enumerare i file all'interno della directory, tranne quando si usano i proxy CERN.</span><span class="sxs-lookup"><span data-stu-id="33fa8-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="33fa8-198">Per ulteriori informazioni su [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), vedere la pagina relativa alla [lettura di file](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="33fa8-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="33fa8-199">Per ulteriori informazioni su [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), vedere [la pagina relativa alla ricerca del file successivo](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="33fa8-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="33fa8-200">Per le applicazioni che devono funzionare tramite un proxy CERN, è possibile usare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per accedere a directory e file FTP.</span><span class="sxs-lookup"><span data-stu-id="33fa8-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="33fa8-201">Le richieste FTP sono incluse in un pacchetto per essere visualizzate come una richiesta HTTP, che verrà accettata dal proxy CERN.</span><span class="sxs-lookup"><span data-stu-id="33fa8-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="33fa8-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato dalla funzione [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e l'URL della risorsa.</span><span class="sxs-lookup"><span data-stu-id="33fa8-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="33fa8-203">L'URL deve includere lo schema (http:, FTP:, file: \[ per un file locale \] o https: \[ per il protocollo Hypertext Secure \] ) e il percorso di rete (ad esempio `www.microsoft.com` ).</span><span class="sxs-lookup"><span data-stu-id="33fa8-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="33fa8-204">L'URL può includere anche un percorso (ad esempio,/ISAPI/gomscom.asp? TARGET =/Windows/Feature/) e il nome della risorsa (ad esempio, default.htm).</span><span class="sxs-lookup"><span data-stu-id="33fa8-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="33fa8-205">Per le richieste HTTP o HTTPS, è possibile includere intestazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="33fa8-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="33fa8-206">[**La InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo URL http o HTTPS) possono usare l'handle creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per scaricare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="33fa8-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="33fa8-207">Il diagramma seguente illustra gli handle da usare con ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="33fa8-207">The following diagram illustrates which handles to use with each function.</span></span>

![handle da usare con le funzioni](images/ax-wnt02.png)

<span data-ttu-id="33fa8-209">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice creato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) viene usato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="33fa8-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="33fa8-210">L'handle **HINTERNET** creato da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) può essere usato da [**la InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (non mostrato qui) e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (solo URL http o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="33fa8-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="33fa8-211">Per altre informazioni, vedere [**handle hInternet**](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="33fa8-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="33fa8-212">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="33fa8-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="33fa8-213">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="33fa8-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="33fa8-214">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="33fa8-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 