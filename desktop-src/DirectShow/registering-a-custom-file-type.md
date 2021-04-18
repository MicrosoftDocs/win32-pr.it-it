---
description: In questo articolo viene descritto il modo in cui il gestore del grafico dei filtri individua un filtro di origine, dato un nome file.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrazione di un tipo di file personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303900"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="902d5-103">Registrazione di un tipo di file personalizzato</span><span class="sxs-lookup"><span data-stu-id="902d5-103">Registering a Custom File Type</span></span>

<span data-ttu-id="902d5-104">In questo articolo viene descritto il modo in cui il gestore del grafico dei filtri individua un filtro di origine, dato un nome file.</span><span class="sxs-lookup"><span data-stu-id="902d5-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="902d5-105">È possibile utilizzare questo meccanismo per registrare i tipi di file personalizzati.</span><span class="sxs-lookup"><span data-stu-id="902d5-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="902d5-106">Una volta registrato il tipo di file, DirectShow caricherà automaticamente il filtro di origine corretto ogni volta che un'applicazione chiama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="902d5-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="902d5-107">Overview</span><span class="sxs-lookup"><span data-stu-id="902d5-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="902d5-108">Protocolli</span><span class="sxs-lookup"><span data-stu-id="902d5-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="902d5-109">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="902d5-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="902d5-110">Byte di controllo</span><span class="sxs-lookup"><span data-stu-id="902d5-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="902d5-111">Caricamento del filtro di origine</span><span class="sxs-lookup"><span data-stu-id="902d5-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="902d5-112">Tipi di file personalizzati in Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="902d5-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="902d5-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="902d5-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="902d5-114">Panoramica</span><span class="sxs-lookup"><span data-stu-id="902d5-114">Overview</span></span>

<span data-ttu-id="902d5-115">Per individuare un filtro di origine da un nome file specificato, il gestore del grafico del filtro tenta di eseguire le operazioni seguenti, nell'ordine indicato:</span><span class="sxs-lookup"><span data-stu-id="902d5-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="902d5-116">Trovare la corrispondenza con il protocollo, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="902d5-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="902d5-117">Corrisponde all'estensione del file.</span><span class="sxs-lookup"><span data-stu-id="902d5-117">Match the file extension.</span></span>
3.  <span data-ttu-id="902d5-118">Corrisponde ai modelli di byte all'interno del file, detti *Check bytes*.</span><span class="sxs-lookup"><span data-stu-id="902d5-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="902d5-119">Protocolli</span><span class="sxs-lookup"><span data-stu-id="902d5-119">Protocols</span></span>

<span data-ttu-id="902d5-120">I nomi di protocollo, ad esempio "FTP" o "http", sono registrati nel</span><span class="sxs-lookup"><span data-stu-id="902d5-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="902d5-121">**\_radice delle classi HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="902d5-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="902d5-122">chiave, con la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="902d5-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="902d5-123">Se il nome file o l'URL contiene i due punti (':'), il gestore del grafico del filtro tenta di utilizzare la parte prima di ':' come nome di protocollo.</span><span class="sxs-lookup"><span data-stu-id="902d5-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="902d5-124">Se, ad esempio, il nome è "myprot://myfile.ext", viene eseguita la ricerca di una chiave del registro di sistema denominata **prot**.</span><span class="sxs-lookup"><span data-stu-id="902d5-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="902d5-125">Se questa chiave esiste e contiene una sottochiave denominata "Extensions", il gestore del grafo dei filtri Cerca le voci che corrispondono all'estensione di file nella sottochiave.</span><span class="sxs-lookup"><span data-stu-id="902d5-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="902d5-126">Il valore della chiave deve essere un GUID in formato stringa. ad esempio, " {00000000-0000-0000-0000-000000000000} ".</span><span class="sxs-lookup"><span data-stu-id="902d5-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="902d5-127">Se il gestore del grafo del filtro non può corrispondere ad alcun elemento all'interno della sottochiave **Extensions** , Cerca una sottochiave denominata **Filter di origine**, che deve essere anche un GUID in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="902d5-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="902d5-128">Se il gestore del grafo del filtro trova un GUID corrispondente, lo utilizza come CLSID del filtro di origine e tenta di caricare il filtro.</span><span class="sxs-lookup"><span data-stu-id="902d5-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="902d5-129">Se non trova una corrispondenza, usa il filtro di [origine file (URL)](file-source--url--filter.md) , che considera il nome del file come un URL.</span><span class="sxs-lookup"><span data-stu-id="902d5-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="902d5-130">Questo algoritmo presenta due eccezioni:</span><span class="sxs-lookup"><span data-stu-id="902d5-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="902d5-131">Per escludere le lettere di driver, le stringhe a carattere singolo non vengono considerate protocolli.</span><span class="sxs-lookup"><span data-stu-id="902d5-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="902d5-132">Se la stringa è "file:" o "file://", non viene considerata come un protocollo.</span><span class="sxs-lookup"><span data-stu-id="902d5-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="902d5-133">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="902d5-133">File Extensions</span></span>

<span data-ttu-id="902d5-134">Se non è presente alcun protocollo nel nome del file, il gestore del grafico dei filtri Cerca nel registro di sistema le voci con le principali **\_ \_ \\ \\ estensioni \\ del tipo di supporto radice delle classi HKEY**.*EXT* \\ , dove.*EXT* è l'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="902d5-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="902d5-135">Se questa chiave esiste, il **filtro di origine** del valore contiene il CLSID del filtro di origine, in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="902d5-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="902d5-136">Facoltativamente, la chiave può avere valori per il **tipo di supporto** e il **sottotipo**, che assegnano al tipo principale e ai GUID del sottotipo.</span><span class="sxs-lookup"><span data-stu-id="902d5-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="902d5-137">Byte di controllo</span><span class="sxs-lookup"><span data-stu-id="902d5-137">Check Bytes</span></span>

<span data-ttu-id="902d5-138">Alcuni tipi di file possono essere identificati da modelli specifici di bit che si verificano in offset di byte specifici nel file.</span><span class="sxs-lookup"><span data-stu-id="902d5-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="902d5-139">Filter Graph Manager cerca le chiavi nel registro di sistema con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="902d5-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="902d5-140">**HKEY \_ Classi \_ radice \\ mediaType \\**{ *tipo principale* } \\ { *sottotipo* }</span><span class="sxs-lookup"><span data-stu-id="902d5-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="902d5-141">dove il *tipo principale* e il *sottotipo* sono GUID che definiscono il tipo di supporto per il flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="902d5-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="902d5-142">Ogni chiave contiene una o più sottochiavi, in genere denominate 1, 2 e così via, che definiscono i byte di controllo; e una sottochiave denominata **filtro di origine** che fornisce il CLSID del filtro di origine, in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="902d5-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="902d5-143">Le sottochiavi di byte di controllo sono stringhe che contengono uno o più quad di numeri chiamati:</span><span class="sxs-lookup"><span data-stu-id="902d5-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="902d5-144">*offset*, *CB*, *mask*, *Val*</span><span class="sxs-lookup"><span data-stu-id="902d5-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="902d5-145">Per trovare la corrispondenza con il file, il gestore del grafo del filtro legge i byte CB, a partire dall'offset del numero di byte.</span><span class="sxs-lookup"><span data-stu-id="902d5-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="902d5-146">Esegue quindi un operatore and bit per bit sul valore in mask.</span><span class="sxs-lookup"><span data-stu-id="902d5-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="902d5-147">Se il risultato è uguale a Val, il file corrisponde a tale quad.</span><span class="sxs-lookup"><span data-stu-id="902d5-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="902d5-148">I valori mask e Val sono specificati in esadecimale.</span><span class="sxs-lookup"><span data-stu-id="902d5-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="902d5-149">Una voce vuota per la maschera viene considerata come una stringa di 1s di lunghezza CB.</span><span class="sxs-lookup"><span data-stu-id="902d5-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="902d5-150">Un valore negativo per offset indica un offset dalla fine del file.</span><span class="sxs-lookup"><span data-stu-id="902d5-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="902d5-151">Per trovare la corrispondenza con la chiave, il file deve corrispondere a tutti i quad in una qualsiasi delle sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="902d5-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="902d5-152">Si supponga, ad esempio, che il registro di sistema contenga le chiavi seguenti in **HKCR \\ Media Type**:</span><span class="sxs-lookup"><span data-stu-id="902d5-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="902d5-153">La prima chiave corrisponde al tipo principale flusso MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="902d5-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="902d5-154">Sottochiave seguente che corrisponde al sottotipo MEDIATYPE \_ MIDI.</span><span class="sxs-lookup"><span data-stu-id="902d5-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="902d5-155">Il valore della sottochiave del filtro di origine è CLSID \_ AsyncReader, il CLSID del filtro di [origine file (Async)](file-source--async--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="902d5-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="902d5-156">Ogni voce può avere più quadruple; tutte devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="902d5-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="902d5-157">Nell'esempio seguente, i primi 4 byte del file devono essere 0xAB, 0xCD, 0x12, 0x34; e gli ultimi 4 byte del file devono essere 0xAB, 0xAB, 0x00, 0xAB:</span><span class="sxs-lookup"><span data-stu-id="902d5-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="902d5-158">Inoltre, possono essere presenti più voci in un unico tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="902d5-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="902d5-159">È sufficiente una corrispondenza con uno di essi.</span><span class="sxs-lookup"><span data-stu-id="902d5-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="902d5-160">Questo schema consente un set di maschere alternative. ad esempio, i file con estensione wav che possono o non possono avere un'intestazione RIFF.</span><span class="sxs-lookup"><span data-stu-id="902d5-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="902d5-161">Questo schema è simile a quello usato dalla funzione [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .</span><span class="sxs-lookup"><span data-stu-id="902d5-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="902d5-162">Caricamento del filtro di origine</span><span class="sxs-lookup"><span data-stu-id="902d5-162">Loading the Source Filter</span></span>

<span data-ttu-id="902d5-163">Supponendo che Filter Graph Manager trovi un filtro di origine corrispondente per il file, aggiunge tale filtro al grafo, esegue una query sul filtro per l'interfaccia [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) e chiama [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span><span class="sxs-lookup"><span data-stu-id="902d5-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="902d5-164">Gli argomenti per il metodo **Load** sono il nome del file e il tipo di supporto, come determinato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="902d5-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="902d5-165">Se il gestore del grafo del filtro non riesce a trovare nulla dal registro di sistema, per impostazione predefinita viene usato il filtro di origine file asincrono.</span><span class="sxs-lookup"><span data-stu-id="902d5-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="902d5-166">In tal caso, imposta il tipo di supporto su **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ None**.</span><span class="sxs-lookup"><span data-stu-id="902d5-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="902d5-167">Tipi di file personalizzati in Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="902d5-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="902d5-168">Windows Media Player utilizza un set aggiuntivo di voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="902d5-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="902d5-169">Per ulteriori informazioni, vedere [impostazioni del registro di sistema](../wmp/file-name-extension-registry-settings.md) per l'estensione di file in Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="902d5-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="902d5-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="902d5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="902d5-171">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="902d5-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 
