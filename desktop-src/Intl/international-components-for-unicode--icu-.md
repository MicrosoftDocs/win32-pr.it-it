---
description: International Components for Unicode (ICU) è un set maturo e ampiamente usato di API di globalizzazione open source.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: International Components for Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7fec661b24e352c24abddf687e6b119752e39ce80c12dc409000afa179f1f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107026"
---
# <a name="international-components-for-unicode-icu"></a>International Components for Unicode (ICU)

International Components for Unicode (ICU) è un set maturo e ampiamente usato di API di globalizzazione open source. ICU usa common locale data repository (CLDR) di Unicode come libreria di dati, fornendo il supporto della globalizzazione per le applicazioni software. L'unità di cu è ampiamente portabile e offre alle applicazioni gli stessi risultati in tutte le piattaforme.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Evidenziazioni dei servizi API Globalizzazione forniti dalla cucu

-   **Conversione tabella codici:** converte i dati di testo in o da Unicode e quasi qualsiasi altro set di caratteri o codifica. Le tabelle di conversione dell'unità di cu sono basate sui dati dei set di caratteri raccolti da IBM nel corso di molti decenni ed è la più completa disponibile ovunque.
-   **Regole di confronto:** confrontare le stringhe in base alle convenzioni e agli standard di una determinata lingua, area geografica o paese. Le regole di confronto dell'unità di compatibilità si basano sull'algoritmo di confronto Unicode e sulle regole di confronto specifiche delle impostazioni locali di CLDR.
-   **Formattazione:** formattare numeri, date, ore e importi di valuta in base alle convenzioni delle impostazioni locali scelte. Ciò include la conversione dei nomi di mese e giorno nella lingua selezionata, la scelta delle abbreviazioni appropriate, l'ordinamento corretto dei campi e così via. Questi dati provengono anche dal repository dei dati delle impostazioni locali comuni.
-   **Calcoli dell'ora:** vengono forniti più tipi di calendari oltre al gregoriano tradizionale. Viene fornito un set completo di API di calcolo del fuso orario.
-   **Supporto Unicode:** CU tiene traccia dello standard Unicode, offrendo un facile accesso a tutte le numerose proprietà dei caratteri Unicode, normalizzazione Unicode, case folding e altre operazioni fondamentali, come specificato dallo [standard Unicode](https://www.unicode.org/).
-   **Espressione regolare:** le espressioni regolari di ICU supportano completamente Unicode e offrono prestazioni molto competitive.
-   **Offeri:** supporto per la gestione di testo contenente una combinazione di dati da sinistra a destra (inglese) e da destra a sinistra (arabo o ebraico).

Per altre informazioni, visitare il sito Web ICU: <http://site.icu-project.org/>

## <a name="overview"></a>Panoramica

In Windows 10 Creators Update, la cu è stata integrata in Windows, rendendo accessibili pubblicamente le API e i dati C.

> [!IMPORTANT]
> La versione del cu in Windows espone solo le API C. Non espone alcuna API C++. Sfortunatamente, non è possibile esporre mai le API C++ a causa della mancanza di un'interfaccia ABI stabile in C++.

Per la documentazione sulle API ICU C, vedere la pagina ufficiale della documentazione dell'unità di cu qui: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Cronologia delle modifiche apportate alla libreria ICU in Windows

### <a name="version-1703-creators-update"></a>Versione 1703 (Creators Update)
La libreria ICU è stata aggiunta per la prima volta Windows 10 sistema operativo in questa versione.
È stato aggiunto come:
- Due DLL di sistema:
    -   **icuuc.dll** (questa è la libreria "comune" dell'unità di cu)
    -   **icuin.dll** (si tratta della libreria ICU "i18n")
- Due file di intestazione nell'SDK Windows 10:
    -   **icucommon.h**
    -   **icui18n.h**
- Due librerie di importazione in Windows 10 SDK:
    -   **icuuc.lib**
    -   **icuin.lib**

### <a name="version-1709-fall-creators-update"></a>Versione 1709 (Fall Creators Update)
È stato aggiunto un file di intestazione combinato, **icu.h,** che contiene il contenuto di entrambi i file di intestazione precedenti (icucommon.h e icui18n.h) e modifica anche il tipo di `UCHAR` in `char16_t` .

### <a name="version-1903-may-2019-update"></a>Versione 1903 (aggiornamento di maggio 2019)
È stata aggiunta una nuova DLL **combinata,icu.dll**, che contiene le librerie "common" e "i18n". Inoltre, è stata aggiunta una nuova libreria di importazione all'SDK Windows 10: **icu.lib**.

In futuro, non verranno aggiunte nuove API alle intestazioni (icucommon.h e icui18n.h) o alle librerie di importazione (icuuc.lib e icuin.lib). Le nuove API verranno aggiunte solo all'intestazione combinata (icu.h) e alla libreria di importazione combinata (icu.lib).

## <a name="getting-started"></a>Introduzione

È necessario eseguire tre passaggi principali: (Windows 10 Creators Update o versione successiva)

<dl>

1. L'applicazione deve essere Windows 10 versione 1703 (Creators Update) o successiva.

2. Aggiungere nelle intestazioni:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   Nella Windows 10 versione 1709 e successive è invece necessario includere l'intestazione combinata:

   ``` syntax
   #include <icu.h>
   ```
  
3. Collegamento alle due librerie:

   -   icuuc.lib
   -   icuin.lib

   Nella Windows 10 versione 1903 e successive è consigliabile usare invece la libreria combinata:

   -   icu.lib

</dl>

È quindi possibile chiamare qualsiasi API C ICU da queste librerie desiderate. Non vengono esposte API C++.

> [!IMPORTANT]
> Se si usano le librerie di importazione legacy, icuuc.lib e icuin.lib, assicurarsi che siano elencate prima delle librerie umbrella, ad esempio onecoreuap.lib o WindowsApp.lib, nell'impostazione Del linker Dipendenze aggiuntive (vedere l'immagine seguente). In caso contrario, il linker si collega a icu.lib, che comporta un tentativo di caricamento icu.dll in fase di esecuzione. Tale DLL è presente solo a partire dalla versione 1903. Pertanto, se un utente aggiorna Windows 10 SDK in un computer Windows precedente alla versione 1903, l'app non verrà caricata ed eseguita. Per una cronologia delle librerie ICU in Windows, vedere Cronologia delle modifiche apportate alla libreria [ICU in Windows](#history-of-changes-to-the-icu-library-in-windows).

![Esempio di icu](images/icu-example.png)

> [!Note]  
>
> - Questa è la configurazione per "Tutte le piattaforme".
> - Per fare in modo che le app Win32 usino la cu, devono chiamare [prima CoInitializeEx.](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) Nella Windows 10 1903 e versioni successive, in cui è disponibile la libreria ICU combinata (icu.dll/icu.lib), è possibile omettere la chiamata CoInitializeEx usando la libreria combinata.
> - Non tutti i dati restituiti dalle API di cu verranno allineati al sistema operativo Windows, perché questo allineamento è ancora in corso. 

## <a name="icu-example-app"></a>App di esempio ICU

### <a name="example-code-snippet"></a>Frammento di codice di esempio

Di seguito è riportato un esempio che illustra l'uso delle API ICU da un'applicazione UWP C++. Non deve essere un'applicazione autonoma completa, ma è solo un esempio di chiamata a un metodo di descrizione dei dati.

Nell'esempio seguente si presuppone che siano disponibili metodi **ErrorMessage** e **OutputMessage** che rendono le stringhe all'utente in qualche modo.

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

 

 



