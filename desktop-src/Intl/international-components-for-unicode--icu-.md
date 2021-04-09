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
# <a name="international-components-for-unicode-icu"></a>International Components for Unicode (ICU)

International Components for Unicode (ICU) è un set di API di globalizzazione Open Source ampiamente usato. ICU usa il repository dei dati delle impostazioni locali (CLDR) di Unicode come raccolta dati, offrendo supporto per la globalizzazione per le applicazioni software. ICU è molto portatile e offre alle applicazioni gli stessi risultati in tutte le piattaforme.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Highlights of the Globalization servizi API fornito da ICU

-   **Conversione della tabella codici**: converte i dati di testo in o da Unicode e quasi qualsiasi altro set di caratteri o codifica. Le tabelle di conversione di ICU sono basate sui dati del set di caratteri raccolti da IBM nel corso di molti decenni ed è il più completo disponibile ovunque.
-   **Regole di confronto**: confrontare le stringhe in base alle convenzioni e agli standard di una lingua, un'area o un paese specifico. Le regole di confronto di ICU sono basate sull'algoritmo di confronto Unicode più le regole di confronto specifiche delle impostazioni locali di CLDR.
-   **Formattazione**: formattare numeri, date, ore e importi di valuta in base alle convenzioni delle impostazioni locali selezionate. Questo include la traduzione dei nomi di mese e giorno nella lingua selezionata, la scelta delle abbreviazioni appropriate, l'ordinamento corretto dei campi e così via. Questi dati provengono anche dal repository di dati delle impostazioni locali comuni.
-   **Calcoli temporali**: vengono forniti più tipi di calendario oltre il gregoriano tradizionale. Viene fornito un set completo di API per il calcolo del fuso orario.
-   **Supporto Unicode**: ICU monitora strettamente lo standard Unicode, semplificando l'accesso a tutte le numerose proprietà dei caratteri Unicode, alla normalizzazione Unicode, alla riduzione dei maiuscole e minuscole e ad altre operazioni fondamentali come specificato dallo [standard Unicode](https://www.unicode.org/).
-   **Espressione regolare**: le espressioni regolari di ICU supportano completamente Unicode offrendo prestazioni molto competitive.
-   **BiDi**: supporto per la gestione di testo che contiene una combinazione di dati da sinistra a destra (Inglese) e da destra a sinistra (arabo o ebraico).

Per ulteriori informazioni, è possibile visitare il sito Web di ICU: <http://site.icu-project.org/>

## <a name="overview"></a>Panoramica

In Windows 10 Creators Update, ICU è stato integrato in Windows, rendendo accessibili pubblicamente le API C e i dati.

> [!IMPORTANT]
> La versione di ICU in Windows espone solo le API C. Non espone alcuna API C++. Sfortunatamente, non è possibile esporre le API C++ a causa della mancanza di un'ABI stabile in C++.

Per la documentazione sulle API di ICU C, consultare la pagina della documentazione di ICU ufficiale qui: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Cronologia delle modifiche apportate alla libreria ICU in Windows

### <a name="version-1703-creators-update"></a>Versione 1703 (Creators Update)
La libreria ICU è stata aggiunta per la prima volta al sistema operativo Windows 10 in questa versione.
È stato aggiunto come:
- Due dll di sistema:
    -   **icuuc.dll** (la libreria "Common" di ICU)
    -   **icuin.dll** (la libreria "i18n" di ICU)
- Due file di intestazione in Windows 10 SDK:
    -   **icucommon. h**
    -   **icui18n. h**
- Due librerie di importazione in Windows 10 SDK:
    -   **icuuc. lib**
    -   **icuin. lib**

### <a name="version-1709-fall-creators-update"></a>Versione 1709 (Fall Creators Update)
È stato aggiunto un file di intestazione combinato, **ICU. h**, che contiene il contenuto di entrambi i file di intestazione sopra (icucommon. h e icui18n. h) e modifica anche il tipo di `UCHAR` in `char16_t` .

### <a name="version-1903-may-2019-update"></a>Versione 1903 (aggiornamento di maggio 2019)
È stata aggiunta una nuova DLL combinata, **icu.dll**, che contiene le librerie "Common" e "i18n". È stata inoltre aggiunta una nuova libreria di importazione a Windows 10 SDK: **ICU. lib**.

In futuro, non verranno aggiunte nuove API alle intestazioni precedenti (icucommon. h e icui18n. h) o alle librerie di importazione precedenti (icuuc. lib e icuin. lib). Le nuove API verranno aggiunte solo all'intestazione combinata (ICU. h) e alla libreria di importazione combinata (ICU. lib).

## <a name="getting-started"></a>Introduzione

È necessario seguire tre passaggi principali: (Windows 10 Creators Update o versione successiva)

<dl>

1. È necessario che l'applicazione sia destinata a Windows 10 versione 1703 (Creators Update) o successiva.

2. Aggiungere le intestazioni:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   In Windows 10 versione 1709 e successive, è necessario includere invece l'intestazione combinata:

   ``` syntax
   #include <icu.h>
   ```
  
3. Collegamento alle due librerie:

   -   icuuc. lib
   -   icuin. lib

   In Windows 10 versione 1903 e successive, è consigliabile usare invece la libreria combinata:

   -   ICU. lib

</dl>

Quindi, è possibile chiamare qualsiasi API di ICU C da queste librerie desiderate. (Nessuna API C++ esposta).

> [!IMPORTANT]
> Se si usano le librerie di importazione legacy, icuuc. lib e icuin. lib, assicurarsi che siano elencate prima delle librerie Umbrella, ad esempio onecoreuap. lib o WindowsApp. lib, nell'impostazione del linker dipendenze aggiuntive (vedere l'immagine seguente). In caso contrario, il linker verrà collegato a ICU. lib, il che comporterà il tentativo di caricare icu.dll in fase di esecuzione. Tale DLL è presente solo a partire dalla versione 1903. Se quindi un utente aggiorna Windows 10 SDK in un computer Windows precedente alla versione 1903, l'app non verrà caricata ed eseguita. Per una cronologia delle librerie di ICU in Windows, vedere [cronologia delle modifiche apportate alla libreria ICU in Windows](#history-of-changes-to-the-icu-library-in-windows).

![esempio di ICU](images/icu-example.png)

> [!Note]  
>
> - Si tratta della configurazione per "tutte le piattaforme".
> - Per usare ICU, le app Win32 devono chiamare prima [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .
> - Non tutti i dati restituiti dalle API di ICU si allineano al sistema operativo Windows, perché il lavoro di allineamento è ancora in corso. 

## <a name="icu-example-app"></a>App di esempio ICU

### <a name="example-code-snippet"></a>Frammento di codice di esempio

Di seguito è riportato un esempio che illustra l'uso delle API di ICU dall'interno di un'applicazione C++ UWP. (Non è destinato a essere un'applicazione autonoma completa, ma è solo un esempio di chiamata a un metodo ICU).

Nel piccolo esempio seguente si presuppone che esistano metodi **ErrorMessage** e **OutputMessage** che restituiscono le stringhe all'utente in un certo modo.

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

 

 



