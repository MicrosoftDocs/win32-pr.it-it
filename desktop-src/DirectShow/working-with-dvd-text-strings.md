---
description: Utilizzo di stringhe di testo DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Utilizzo di stringhe di testo DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308937"
---
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="122d4-103">Utilizzo di stringhe di testo DVD</span><span class="sxs-lookup"><span data-stu-id="122d4-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="122d4-104">Alcuni dischi DVD, in particolare i dischi Karaoke, possono contenere un elenco di stringhe di testo per integrare il contenuto video o audio.</span><span class="sxs-lookup"><span data-stu-id="122d4-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="122d4-105">Queste stringhe di testo contengono metadati sul contenuto, ad esempio titoli di canzoni, nomi di artisti, informazioni sul genere e così via.</span><span class="sxs-lookup"><span data-stu-id="122d4-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="122d4-106">Le stringhe di testo possono essere presenti in più di una lingua.</span><span class="sxs-lookup"><span data-stu-id="122d4-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="122d4-107">Queste stringhe sono facoltative e molti dischi non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="122d4-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="122d4-108">Per recuperare le stringhe di testo da un DVD, usare l'interfaccia [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , esposta dal [navigatore DVD](dvd-navigator-filter.md).</span><span class="sxs-lookup"><span data-stu-id="122d4-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="122d4-109">In realtà non è necessario creare un grafico di riproduzione DVD per recuperare le stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="122d4-110">È sufficiente creare il navigatore DVD, impostare il volume DVD e quindi chiamare i metodi di stringa di testo pertinenti:</span><span class="sxs-lookup"><span data-stu-id="122d4-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="122d4-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="122d4-111">Method</span></span>                                                                                  | <span data-ttu-id="122d4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="122d4-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="122d4-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="122d4-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="122d4-114">Ottiene il numero di lingue per cui sono presenti stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="122d4-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span><span class="sxs-lookup"><span data-stu-id="122d4-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="122d4-116">Ottiene informazioni sulle stringhe di testo per una lingua.</span><span class="sxs-lookup"><span data-stu-id="122d4-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="122d4-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span><span class="sxs-lookup"><span data-stu-id="122d4-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="122d4-118">Ottiene una stringa di testo per una lingua specificata, in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="122d4-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="122d4-119">**IDvdInfo2::GetDVDTextStringAsNative**</span><span class="sxs-lookup"><span data-stu-id="122d4-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="122d4-120">Ottiene una stringa di testo come matrice di byte non elaborata.</span><span class="sxs-lookup"><span data-stu-id="122d4-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="122d4-121">Utilizzare questo metodo se la stringa di testo utilizza una codifica dei caratteri non supportata da [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span><span class="sxs-lookup"><span data-stu-id="122d4-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="122d4-122">Di seguito è riportata la procedura di base per ottenere le stringhe di testo:</span><span class="sxs-lookup"><span data-stu-id="122d4-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="122d4-123">Chiamare [**IDvdInfo2:: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) per trovare il numero totale di lingue in cui vengono visualizzate le stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="122d4-124">Se il numero è zero, significa che il DVD non contiene stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="122d4-125">Questo è probabilmente il caso più comune, infatti.</span><span class="sxs-lookup"><span data-stu-id="122d4-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="122d4-126">Se il numero di lingue è almeno uno, chiamare [**IDvdInfo2:: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) per ottenere informazioni su ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="122d4-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="122d4-127">Il linguaggio è specificato dall'indice.</span><span class="sxs-lookup"><span data-stu-id="122d4-127">The language is specified by index.</span></span> <span data-ttu-id="122d4-128">Il metodo restituisce il numero totale di stringhe di testo in tale lingua, l'identificatore delle impostazioni locali (**LCID**) per la lingua e la codifica dei caratteri (Unicode o other).</span><span class="sxs-lookup"><span data-stu-id="122d4-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="122d4-129">Le stringhe di testo DVD possono usare diversi set di caratteri diversi. sono elencate in [**DVD \_ TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span><span class="sxs-lookup"><span data-stu-id="122d4-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="122d4-130">Per ottenere una stringa di testo, chiamare [**IDvdInfo2:: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) o [**IDvdInfo2:: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span><span class="sxs-lookup"><span data-stu-id="122d4-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="122d4-131">Il primo metodo restituisce una stringa di caratteri wide, ma non supporta tutti i set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="122d4-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="122d4-132">Il secondo metodo restituisce una matrice di byte che contiene i dati di testo non elaborati.</span><span class="sxs-lookup"><span data-stu-id="122d4-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="122d4-133">Per entrambi i metodi, è possibile chiamare il metodo con un puntatore del buffer **null** per trovare la dimensione della stringa e il tipo di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="122d4-134">Quindi allocare un buffer e chiamare di nuovo il metodo per ottenere la stringa.</span><span class="sxs-lookup"><span data-stu-id="122d4-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="122d4-135">A ogni stringa di testo è associato un codice identificatore, che indica il significato della stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="122d4-136">L'identificatore viene restituito come valore [**\_ TextStringType DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) .</span><span class="sxs-lookup"><span data-stu-id="122d4-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="122d4-137">Esistono due categorie di identificatore: *identificatori di struttura* e *identificatori di contenuto*.</span><span class="sxs-lookup"><span data-stu-id="122d4-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="122d4-138">Gli identificatori di struttura hanno codici numerici nell'intervallo da 0x00 a 0x02F.</span><span class="sxs-lookup"><span data-stu-id="122d4-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="122d4-139">Gli identificatori di contenuto hanno un intervallo di 0x30 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="122d4-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="122d4-140">L'enumerazione **DVD \_ TextStringType** definisce un subset degli identificatori più comuni, ma i metodi [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) possono restituire qualsiasi codice identificatore. Un identificatore di struttura descrive una parte logica del DVD, ad esempio volume, titolo o parte del titolo (PTT).</span><span class="sxs-lookup"><span data-stu-id="122d4-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="122d4-141">Un identificatore del contenuto indica il significato di una determinata stringa di testo, ad esempio titolo del film, titolo del brano o genere.</span><span class="sxs-lookup"><span data-stu-id="122d4-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="122d4-142">Agli identificatori di struttura non sono associate stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="122d4-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="122d4-143">Quando un identificatore di struttura viene visualizzato nei dati della stringa di testo, segnala che le stringhe di testo seguenti si applicano alla parte logica del DVD, fino all'identificatore di struttura successivo.</span><span class="sxs-lookup"><span data-stu-id="122d4-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="122d4-144">La posizione degli identificatori di struttura all'interno dei dati di testo corrisponde alla gerarchia logica del volume DVD.</span><span class="sxs-lookup"><span data-stu-id="122d4-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="122d4-145">Ad esempio, la prima occorrenza dell' \_ identificatore del titolo della struct DVD \_ (0x02) rappresenta il primo titolo del volume e l'occorrenza successiva rappresenta il secondo titolo.</span><span class="sxs-lookup"><span data-stu-id="122d4-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="122d4-146">La tabella seguente illustra in che modo è possibile definire le stringhe di testo per un DVD con due titoli.</span><span class="sxs-lookup"><span data-stu-id="122d4-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="122d4-147">\_TEXTSTRINGTYPE DVD</span><span class="sxs-lookup"><span data-stu-id="122d4-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="122d4-148">Stringa di testo</span><span class="sxs-lookup"><span data-stu-id="122d4-148">Text string</span></span>  | <span data-ttu-id="122d4-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="122d4-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="122d4-150">\_Volume struct DVD \_ (0x01)</span><span class="sxs-lookup"><span data-stu-id="122d4-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="122d4-151">""</span><span class="sxs-lookup"><span data-stu-id="122d4-151">""</span></span>           | <span data-ttu-id="122d4-152">Identificatore della struttura per l'intero lato del disco.</span><span class="sxs-lookup"><span data-stu-id="122d4-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="122d4-153">\_Nome generale DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="122d4-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="122d4-154">"Volume DVD"</span><span class="sxs-lookup"><span data-stu-id="122d4-154">"DVD Volume"</span></span> | <span data-ttu-id="122d4-155">Nome del volume DVD.</span><span class="sxs-lookup"><span data-stu-id="122d4-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="122d4-156">\_Titolo struct DVD \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="122d4-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="122d4-157">""</span><span class="sxs-lookup"><span data-stu-id="122d4-157">""</span></span>           | <span data-ttu-id="122d4-158">Identificatore di struttura per il primo titolo.</span><span class="sxs-lookup"><span data-stu-id="122d4-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="122d4-159">\_Nome generale DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="122d4-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="122d4-160">"Title 1"</span><span class="sxs-lookup"><span data-stu-id="122d4-160">"Title 1"</span></span>    | <span data-ttu-id="122d4-161">Nome del primo titolo.</span><span class="sxs-lookup"><span data-stu-id="122d4-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="122d4-162">\_Titolo struct DVD \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="122d4-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="122d4-163">""</span><span class="sxs-lookup"><span data-stu-id="122d4-163">""</span></span>           | <span data-ttu-id="122d4-164">Identificatore di struttura per il secondo titolo.</span><span class="sxs-lookup"><span data-stu-id="122d4-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="122d4-165">\_Nome generale DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="122d4-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="122d4-166">"Title 2"</span><span class="sxs-lookup"><span data-stu-id="122d4-166">"Title 2"</span></span>    | <span data-ttu-id="122d4-167">Nome del secondo titolo.</span><span class="sxs-lookup"><span data-stu-id="122d4-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="122d4-168">I metodi [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) e [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) considerano gli identificatori di struttura e gli identificatori di contenuto uguali.</span><span class="sxs-lookup"><span data-stu-id="122d4-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="122d4-169">L'unica differenza è che per gli identificatori di struttura il buffer di testo associato è vuoto.</span><span class="sxs-lookup"><span data-stu-id="122d4-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="122d4-170">Spetta all'applicazione tenere traccia della relazione tra le stringhe di testo e le parti logiche del DVD.</span><span class="sxs-lookup"><span data-stu-id="122d4-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="122d4-171">Nell'esempio seguente viene illustrato come ottenere stringhe di testo da un DVD.</span><span class="sxs-lookup"><span data-stu-id="122d4-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="122d4-172">Questo esempio Ignora alcuni dettagli necessari per un'applicazione reale.</span><span class="sxs-lookup"><span data-stu-id="122d4-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="122d4-173">Ad esempio, ignora gli identificatori di struttura. L'esempio ha lo scopo di mostrare solo la sequenza di chiamate corretta.</span><span class="sxs-lookup"><span data-stu-id="122d4-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



<span data-ttu-id="122d4-174">Per informazioni sulle stringhe di testo DVD, vedere il [sito Web del forum](https://go.microsoft.com/fwlink/?LinkId=8677)relativo ai DVD.</span><span class="sxs-lookup"><span data-stu-id="122d4-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="122d4-175">Il metodo **CDvdCore:: GetDvdText** nell'applicazione DVDSample illustra i passaggi di base per l'enumerazione e la visualizzazione delle stringhe di testo DVD.</span><span class="sxs-lookup"><span data-stu-id="122d4-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="122d4-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="122d4-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="122d4-177">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="122d4-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



