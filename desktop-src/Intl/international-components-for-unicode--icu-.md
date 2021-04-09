---
description: International Components for Unicode (ICU) è un set di API di globalizzazione Open Source ampiamente usato.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: International Components for Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00a72885b37efebf8de0d5eb60a22fe01dfba4f
ms.sourcegitcommit: 176ef0a00690f849282cb48464c97f6526a82113
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2021
ms.locfileid: "103968771"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="29425-103">International Components for Unicode (ICU)</span><span class="sxs-lookup"><span data-stu-id="29425-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="29425-104">International Components for Unicode (ICU) è un set di API di globalizzazione Open Source ampiamente usato.</span><span class="sxs-lookup"><span data-stu-id="29425-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="29425-105">ICU usa il repository dei dati delle impostazioni locali (CLDR) di Unicode come raccolta dati, offrendo supporto per la globalizzazione per le applicazioni software.</span><span class="sxs-lookup"><span data-stu-id="29425-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="29425-106">ICU è molto portatile e offre alle applicazioni gli stessi risultati in tutte le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="29425-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="29425-107">Highlights of the Globalization servizi API fornito da ICU</span><span class="sxs-lookup"><span data-stu-id="29425-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="29425-108">**Conversione della tabella codici**: converte i dati di testo in o da Unicode e quasi qualsiasi altro set di caratteri o codifica.</span><span class="sxs-lookup"><span data-stu-id="29425-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="29425-109">Le tabelle di conversione di ICU sono basate sui dati del set di caratteri raccolti da IBM nel corso di molti decenni ed è il più completo disponibile ovunque.</span><span class="sxs-lookup"><span data-stu-id="29425-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="29425-110">**Regole di confronto**: confrontare le stringhe in base alle convenzioni e agli standard di una lingua, un'area o un paese specifico.</span><span class="sxs-lookup"><span data-stu-id="29425-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="29425-111">Le regole di confronto di ICU sono basate sull'algoritmo di confronto Unicode più le regole di confronto specifiche delle impostazioni locali di CLDR.</span><span class="sxs-lookup"><span data-stu-id="29425-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="29425-112">**Formattazione**: formattare numeri, date, ore e importi di valuta in base alle convenzioni delle impostazioni locali selezionate.</span><span class="sxs-lookup"><span data-stu-id="29425-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="29425-113">Questo include la traduzione dei nomi di mese e giorno nella lingua selezionata, la scelta delle abbreviazioni appropriate, l'ordinamento corretto dei campi e così via. Questi dati provengono anche dal repository di dati delle impostazioni locali comuni.</span><span class="sxs-lookup"><span data-stu-id="29425-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="29425-114">**Calcoli temporali**: vengono forniti più tipi di calendario oltre il gregoriano tradizionale.</span><span class="sxs-lookup"><span data-stu-id="29425-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="29425-115">Viene fornito un set completo di API per il calcolo del fuso orario.</span><span class="sxs-lookup"><span data-stu-id="29425-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="29425-116">**Supporto Unicode**: ICU monitora strettamente lo standard Unicode, semplificando l'accesso a tutte le numerose proprietà dei caratteri Unicode, alla normalizzazione Unicode, alla riduzione dei maiuscole e minuscole e ad altre operazioni fondamentali come specificato dallo [standard Unicode](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="29425-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="29425-117">**Espressione regolare**: le espressioni regolari di ICU supportano completamente Unicode offrendo prestazioni molto competitive.</span><span class="sxs-lookup"><span data-stu-id="29425-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="29425-118">**BiDi**: supporto per la gestione di testo che contiene una combinazione di dati da sinistra a destra (Inglese) e da destra a sinistra (arabo o ebraico).</span><span class="sxs-lookup"><span data-stu-id="29425-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="29425-119">Per ulteriori informazioni, è possibile visitare il sito Web di ICU: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="29425-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="29425-120">Panoramica</span><span class="sxs-lookup"><span data-stu-id="29425-120">Overview</span></span>

<span data-ttu-id="29425-121">In Windows 10 Creators Update, ICU è stato integrato in Windows, rendendo accessibili pubblicamente le API C e i dati.</span><span class="sxs-lookup"><span data-stu-id="29425-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29425-122">La versione di ICU in Windows espone solo le API C.</span><span class="sxs-lookup"><span data-stu-id="29425-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="29425-123">Non espone alcuna API C++.</span><span class="sxs-lookup"><span data-stu-id="29425-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="29425-124">Sfortunatamente, non è possibile esporre le API C++ a causa della mancanza di un'ABI stabile in C++.</span><span class="sxs-lookup"><span data-stu-id="29425-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="29425-125">Per la documentazione sulle API di ICU C, consultare la pagina della documentazione di ICU ufficiale qui: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="29425-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="29425-126">Cronologia delle modifiche apportate alla libreria ICU in Windows</span><span class="sxs-lookup"><span data-stu-id="29425-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="29425-127">Versione 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="29425-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="29425-128">La libreria ICU è stata aggiunta per la prima volta al sistema operativo Windows 10 in questa versione.</span><span class="sxs-lookup"><span data-stu-id="29425-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="29425-129">È stato aggiunto come:</span><span class="sxs-lookup"><span data-stu-id="29425-129">It was added as:</span></span>
- <span data-ttu-id="29425-130">Due dll di sistema:</span><span class="sxs-lookup"><span data-stu-id="29425-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="29425-131">**icuuc.dll** (la libreria "Common" di ICU)</span><span class="sxs-lookup"><span data-stu-id="29425-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="29425-132">**icuin.dll** (la libreria "i18n" di ICU)</span><span class="sxs-lookup"><span data-stu-id="29425-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="29425-133">Due file di intestazione in Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="29425-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="29425-134">**icucommon. h**</span><span class="sxs-lookup"><span data-stu-id="29425-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="29425-135">**icui18n. h**</span><span class="sxs-lookup"><span data-stu-id="29425-135">**icui18n.h**</span></span>
- <span data-ttu-id="29425-136">Due librerie di importazione in Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="29425-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="29425-137">**icuuc. lib**</span><span class="sxs-lookup"><span data-stu-id="29425-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="29425-138">**icuin. lib**</span><span class="sxs-lookup"><span data-stu-id="29425-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="29425-139">Versione 1709 (Fall Creators Update)</span><span class="sxs-lookup"><span data-stu-id="29425-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="29425-140">È stato aggiunto un file di intestazione combinato, **ICU. h**, che contiene il contenuto di entrambi i file di intestazione sopra (icucommon. h e icui18n. h) e modifica anche il tipo di `UCHAR` in `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="29425-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="29425-141">Versione 1903 (aggiornamento di maggio 2019)</span><span class="sxs-lookup"><span data-stu-id="29425-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="29425-142">È stata aggiunta una nuova DLL combinata, **icu.dll**, che contiene le librerie "Common" e "i18n".</span><span class="sxs-lookup"><span data-stu-id="29425-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="29425-143">È stata inoltre aggiunta una nuova libreria di importazione a Windows 10 SDK: **ICU. lib**.</span><span class="sxs-lookup"><span data-stu-id="29425-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="29425-144">In futuro, non verranno aggiunte nuove API alle intestazioni precedenti (icucommon. h e icui18n. h) o alle librerie di importazione precedenti (icuuc. lib e icuin. lib).</span><span class="sxs-lookup"><span data-stu-id="29425-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="29425-145">Le nuove API verranno aggiunte solo all'intestazione combinata (ICU. h) e alla libreria di importazione combinata (ICU. lib).</span><span class="sxs-lookup"><span data-stu-id="29425-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="29425-146">Introduzione</span><span class="sxs-lookup"><span data-stu-id="29425-146">Getting Started</span></span>

<span data-ttu-id="29425-147">È necessario seguire tre passaggi principali: (Windows 10 Creators Update o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="29425-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="29425-148">È necessario che l'applicazione sia destinata a Windows 10 versione 1703 (Creators Update) o successiva.</span><span class="sxs-lookup"><span data-stu-id="29425-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="29425-149">Aggiungere le intestazioni:</span><span class="sxs-lookup"><span data-stu-id="29425-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="29425-150">In Windows 10 versione 1709 e successive, è necessario includere invece l'intestazione combinata:</span><span class="sxs-lookup"><span data-stu-id="29425-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="29425-151">Collegamento alle due librerie:</span><span class="sxs-lookup"><span data-stu-id="29425-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="29425-152">icuuc. lib</span><span class="sxs-lookup"><span data-stu-id="29425-152">icuuc.lib</span></span>
   -   <span data-ttu-id="29425-153">icuin. lib</span><span class="sxs-lookup"><span data-stu-id="29425-153">icuin.lib</span></span>

   <span data-ttu-id="29425-154">In Windows 10 versione 1903 e successive, è consigliabile usare invece la libreria combinata:</span><span class="sxs-lookup"><span data-stu-id="29425-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="29425-155">ICU. lib</span><span class="sxs-lookup"><span data-stu-id="29425-155">icu.lib</span></span>

</dl>

<span data-ttu-id="29425-156">Quindi, è possibile chiamare qualsiasi API di ICU C da queste librerie desiderate.</span><span class="sxs-lookup"><span data-stu-id="29425-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="29425-157">(Nessuna API C++ esposta).</span><span class="sxs-lookup"><span data-stu-id="29425-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29425-158">Se si usano le librerie di importazione legacy, icuuc. lib e icuin. lib, assicurarsi che siano elencate prima delle librerie Umbrella, ad esempio onecoreuap. lib o WindowsApp. lib, nell'impostazione del linker dipendenze aggiuntive (vedere l'immagine seguente).</span><span class="sxs-lookup"><span data-stu-id="29425-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="29425-159">In caso contrario, il linker verrà collegato a ICU. lib, il che comporterà il tentativo di caricare icu.dll in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="29425-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="29425-160">Tale DLL è presente solo a partire dalla versione 1903.</span><span class="sxs-lookup"><span data-stu-id="29425-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="29425-161">Se quindi un utente aggiorna Windows 10 SDK in un computer Windows precedente alla versione 1903, l'app non verrà caricata ed eseguita.</span><span class="sxs-lookup"><span data-stu-id="29425-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="29425-162">Per una cronologia delle librerie di ICU in Windows, vedere [cronologia delle modifiche apportate alla libreria ICU in Windows](#history-of-changes-to-the-icu-library-in-windows).</span><span class="sxs-lookup"><span data-stu-id="29425-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![esempio di ICU](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="29425-164">Si tratta della configurazione per "tutte le piattaforme".</span><span class="sxs-lookup"><span data-stu-id="29425-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="29425-165">Per usare ICU, le app Win32 devono chiamare prima [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="29425-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span>
> - <span data-ttu-id="29425-166">Non tutti i dati restituiti dalle API di ICU si allineano al sistema operativo Windows, perché il lavoro di allineamento è ancora in corso.</span><span class="sxs-lookup"><span data-stu-id="29425-166">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="29425-167">App di esempio ICU</span><span class="sxs-lookup"><span data-stu-id="29425-167">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="29425-168">Frammento di codice di esempio</span><span class="sxs-lookup"><span data-stu-id="29425-168">Example code snippet</span></span>

<span data-ttu-id="29425-169">Di seguito è riportato un esempio che illustra l'uso delle API di ICU dall'interno di un'applicazione C++ UWP.</span><span class="sxs-lookup"><span data-stu-id="29425-169">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="29425-170">(Non è destinato a essere un'applicazione autonoma completa, ma è solo un esempio di chiamata a un metodo ICU).</span><span class="sxs-lookup"><span data-stu-id="29425-170">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="29425-171">Nel piccolo esempio seguente si presuppone che esistano metodi **ErrorMessage** e **OutputMessage** che restituiscono le stringhe all'utente in un certo modo.</span><span class="sxs-lookup"><span data-stu-id="29425-171">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

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

 

 



