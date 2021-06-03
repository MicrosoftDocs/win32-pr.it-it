---
description: International Components for Unicode (ICU) è un set maturo e ampiamente usato di API di globalizzazione open source.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: International Components for Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349990"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="2e62c-103">International Components for Unicode (ICU)</span><span class="sxs-lookup"><span data-stu-id="2e62c-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="2e62c-104">International Components for Unicode (ICU) è un set maturo e ampiamente usato di API di globalizzazione open source.</span><span class="sxs-lookup"><span data-stu-id="2e62c-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="2e62c-105">ICU usa common locale data repository (CLDR) di Unicode come libreria di dati, fornendo il supporto della globalizzazione per le applicazioni software.</span><span class="sxs-lookup"><span data-stu-id="2e62c-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="2e62c-106">L'unità di cu è ampiamente portabile e offre alle applicazioni gli stessi risultati in tutte le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="2e62c-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="2e62c-107">Caratteristiche principali dei servizi API Globalizzazione ICU</span><span class="sxs-lookup"><span data-stu-id="2e62c-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="2e62c-108">**Conversione tabella codici:** converte i dati di testo in o da Unicode e quasi qualsiasi altro set di caratteri o codifica.</span><span class="sxs-lookup"><span data-stu-id="2e62c-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="2e62c-109">Le tabelle di conversione dell'unità di cu sono basate sui dati dei set di caratteri raccolti da IBM nel corso di molti decenni ed è la più completa disponibile ovunque.</span><span class="sxs-lookup"><span data-stu-id="2e62c-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="2e62c-110">**Regole di confronto:** confrontare le stringhe in base alle convenzioni e agli standard di una determinata lingua, area geografica o paese.</span><span class="sxs-lookup"><span data-stu-id="2e62c-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="2e62c-111">Le regole di confronto dell'unità di compatibilità si basano sull'algoritmo di confronto Unicode e sulle regole di confronto specifiche delle impostazioni locali di CLDR.</span><span class="sxs-lookup"><span data-stu-id="2e62c-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="2e62c-112">**Formattazione:** formattare numeri, date, ore e importi di valuta in base alle convenzioni delle impostazioni locali scelte.</span><span class="sxs-lookup"><span data-stu-id="2e62c-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="2e62c-113">Ciò include la conversione dei nomi di mese e giorno nella lingua selezionata, la scelta delle abbreviazioni appropriate, l'ordinamento corretto dei campi e così via. Questi dati provengono anche dal repository dei dati delle impostazioni locali comuni.</span><span class="sxs-lookup"><span data-stu-id="2e62c-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="2e62c-114">**Calcoli dell'ora:** vengono forniti più tipi di calendari oltre al gregoriano tradizionale.</span><span class="sxs-lookup"><span data-stu-id="2e62c-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="2e62c-115">Viene fornito un set completo di API di calcolo del fuso orario.</span><span class="sxs-lookup"><span data-stu-id="2e62c-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="2e62c-116">**Supporto Unicode:** CU tiene traccia dello standard Unicode, offrendo un facile accesso a tutte le numerose proprietà dei caratteri Unicode, normalizzazione Unicode, case folding e altre operazioni fondamentali, come specificato dallo [standard Unicode](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="2e62c-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="2e62c-117">**Espressione regolare:** le espressioni regolari di ICU supportano completamente Unicode e offrono prestazioni molto competitive.</span><span class="sxs-lookup"><span data-stu-id="2e62c-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="2e62c-118">**Offeri:** supporto per la gestione di testo contenente una combinazione di dati da sinistra a destra (inglese) e da destra a sinistra (arabo o ebraico).</span><span class="sxs-lookup"><span data-stu-id="2e62c-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="2e62c-119">Per altre informazioni, visitare il sito Web ICU: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="2e62c-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="2e62c-120">Panoramica</span><span class="sxs-lookup"><span data-stu-id="2e62c-120">Overview</span></span>

<span data-ttu-id="2e62c-121">In Windows 10 Creators Update, la cu è stata integrata in Windows, rendendo accessibili pubblicamente le API e i dati C.</span><span class="sxs-lookup"><span data-stu-id="2e62c-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e62c-122">La versione di ICU in Windows espone solo le API C.</span><span class="sxs-lookup"><span data-stu-id="2e62c-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="2e62c-123">Non espone alcuna API C++.</span><span class="sxs-lookup"><span data-stu-id="2e62c-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="2e62c-124">Sfortunatamente, non è possibile esporre mai le API C++ a causa della mancanza di un'interfaccia ABI stabile in C++.</span><span class="sxs-lookup"><span data-stu-id="2e62c-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="2e62c-125">Per la documentazione sulle API ICU C, vedere la pagina ufficiale della documentazione dell'unità di cu qui: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="2e62c-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="2e62c-126">Cronologia delle modifiche apportate alla libreria ICU in Windows</span><span class="sxs-lookup"><span data-stu-id="2e62c-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="2e62c-127">Versione 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="2e62c-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="2e62c-128">La libreria ICU è stata aggiunta per la prima volta Windows 10 sistema operativo in questa versione.</span><span class="sxs-lookup"><span data-stu-id="2e62c-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="2e62c-129">È stato aggiunto come:</span><span class="sxs-lookup"><span data-stu-id="2e62c-129">It was added as:</span></span>
- <span data-ttu-id="2e62c-130">Due DLL di sistema:</span><span class="sxs-lookup"><span data-stu-id="2e62c-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="2e62c-131">**icuuc.dll** (questa è la libreria "comune" di cu)</span><span class="sxs-lookup"><span data-stu-id="2e62c-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="2e62c-132">**icuin.dll** (si tratta della libreria ICU "i18n")</span><span class="sxs-lookup"><span data-stu-id="2e62c-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="2e62c-133">Due file di intestazione in Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="2e62c-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="2e62c-134">**icucommon.h**</span><span class="sxs-lookup"><span data-stu-id="2e62c-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="2e62c-135">**icui18n.h**</span><span class="sxs-lookup"><span data-stu-id="2e62c-135">**icui18n.h**</span></span>
- <span data-ttu-id="2e62c-136">Due librerie di importazione in Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="2e62c-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="2e62c-137">**icuuc.lib**</span><span class="sxs-lookup"><span data-stu-id="2e62c-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="2e62c-138">**icuin.lib**</span><span class="sxs-lookup"><span data-stu-id="2e62c-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="2e62c-139">Versione 1709 (Fall Creators Update)</span><span class="sxs-lookup"><span data-stu-id="2e62c-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="2e62c-140">È stato aggiunto un file di intestazione combinato, **icu.h,** che contiene il contenuto di entrambi i file di intestazione precedenti (icucommon.h e icui18n.h) e modifica anche il tipo di `UCHAR` in `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="2e62c-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="2e62c-141">Versione 1903 (aggiornamento di maggio 2019)</span><span class="sxs-lookup"><span data-stu-id="2e62c-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="2e62c-142">È stata aggiunta una nuova DLL **combinata,icu.dll**, che contiene le librerie "common" e "i18n".</span><span class="sxs-lookup"><span data-stu-id="2e62c-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="2e62c-143">Inoltre, è stata aggiunta una nuova libreria di importazione all'SDK Windows 10: **icu.lib**.</span><span class="sxs-lookup"><span data-stu-id="2e62c-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="2e62c-144">In futuro, non verranno aggiunte nuove API alle intestazioni precedente (icucommon.h e icui18n.h) o alle librerie di importazione (icuuc.lib e icuin.lib).</span><span class="sxs-lookup"><span data-stu-id="2e62c-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="2e62c-145">Le nuove API verranno aggiunte solo all'intestazione combinata (icu.h) e alla libreria di importazione combinata (icu.lib).</span><span class="sxs-lookup"><span data-stu-id="2e62c-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="2e62c-146">Introduzione</span><span class="sxs-lookup"><span data-stu-id="2e62c-146">Getting Started</span></span>

<span data-ttu-id="2e62c-147">È necessario eseguire tre passaggi principali: (Windows 10 Creators Update o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="2e62c-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="2e62c-148">L'applicazione deve essere Windows 10 versione 1703 (Creators Update) o successiva.</span><span class="sxs-lookup"><span data-stu-id="2e62c-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="2e62c-149">Aggiungere nelle intestazioni:</span><span class="sxs-lookup"><span data-stu-id="2e62c-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="2e62c-150">Nella Windows 10 versione 1709 e successive è invece necessario includere l'intestazione combinata:</span><span class="sxs-lookup"><span data-stu-id="2e62c-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="2e62c-151">Collegamento alle due librerie:</span><span class="sxs-lookup"><span data-stu-id="2e62c-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="2e62c-152">icuuc.lib</span><span class="sxs-lookup"><span data-stu-id="2e62c-152">icuuc.lib</span></span>
   -   <span data-ttu-id="2e62c-153">icuin.lib</span><span class="sxs-lookup"><span data-stu-id="2e62c-153">icuin.lib</span></span>

   <span data-ttu-id="2e62c-154">Nella Windows 10 versione 1903 e successive è consigliabile usare invece la libreria combinata:</span><span class="sxs-lookup"><span data-stu-id="2e62c-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="2e62c-155">icu.lib</span><span class="sxs-lookup"><span data-stu-id="2e62c-155">icu.lib</span></span>

</dl>

<span data-ttu-id="2e62c-156">È quindi possibile chiamare qualsiasi API C ICU da queste librerie desiderate.</span><span class="sxs-lookup"><span data-stu-id="2e62c-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="2e62c-157">Non vengono esposte API C++.</span><span class="sxs-lookup"><span data-stu-id="2e62c-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e62c-158">Se si usano le librerie di importazione legacy, icuuc.lib e icuin.lib, assicurarsi che siano elencate prima delle librerie umbrella, ad esempio onecoreuap.lib o WindowsApp.lib, nell'impostazione Del linker Dipendenze aggiuntive (vedere l'immagine seguente).</span><span class="sxs-lookup"><span data-stu-id="2e62c-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="2e62c-159">In caso contrario, il linker si collega a icu.lib, il che comporta un tentativo di caricamento icu.dll in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2e62c-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="2e62c-160">Tale DLL è presente solo a partire dalla versione 1903.</span><span class="sxs-lookup"><span data-stu-id="2e62c-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="2e62c-161">Pertanto, se un utente aggiorna Windows 10 SDK in un computer Windows precedente alla versione 1903, l'app non verrà caricata ed eseguita.</span><span class="sxs-lookup"><span data-stu-id="2e62c-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="2e62c-162">Per una cronologia delle librerie ICU in Windows, vedere Cronologia delle modifiche apportate alla libreria di unità [di cu in Windows.](#history-of-changes-to-the-icu-library-in-windows)</span><span class="sxs-lookup"><span data-stu-id="2e62c-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![Esempio di icu](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="2e62c-164">Questa è la configurazione per "Tutte le piattaforme".</span><span class="sxs-lookup"><span data-stu-id="2e62c-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="2e62c-165">Per fare in modo che le app Win32 usino la cu, devono chiamare [prima CoInitializeEx.](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="2e62c-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span> <span data-ttu-id="2e62c-166">Nella Windows 10 versione 1903 e successive, in cui è disponibile la libreria ICU combinata (icu.dll/icu.lib), è possibile omettere la chiamata CoInitializeEx usando la libreria combinata.</span><span class="sxs-lookup"><span data-stu-id="2e62c-166">On Windows 10 version 1903 and above, where the combined ICU library (icu.dll/icu.lib) is available, you can omit the CoInitializeEx call by using the combined library.</span></span>
> - <span data-ttu-id="2e62c-167">Non tutti i dati restituiti dalle API di cu verranno allineati con il sistema operativo Windows, perché il lavoro di allineamento è ancora in corso.</span><span class="sxs-lookup"><span data-stu-id="2e62c-167">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="2e62c-168">App di esempio ICU</span><span class="sxs-lookup"><span data-stu-id="2e62c-168">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="2e62c-169">Frammento di codice di esempio</span><span class="sxs-lookup"><span data-stu-id="2e62c-169">Example code snippet</span></span>

<span data-ttu-id="2e62c-170">Di seguito è riportato un esempio che illustra l'uso delle API ICU da un'applicazione UWP C++.</span><span class="sxs-lookup"><span data-stu-id="2e62c-170">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="2e62c-171">Non deve essere un'applicazione autonoma completa, ma è solo un esempio di chiamata a un metodo di descrizione dei cu.</span><span class="sxs-lookup"><span data-stu-id="2e62c-171">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="2e62c-172">Nell'esempio seguente si presuppone che siano presenti metodi **ErrorMessage** e **OutputMessage** che rendono le stringhe all'utente in qualche modo.</span><span class="sxs-lookup"><span data-stu-id="2e62c-172">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



