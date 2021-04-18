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
# <a name="working-with-dvd-text-strings"></a>Utilizzo di stringhe di testo DVD

Alcuni dischi DVD, in particolare i dischi Karaoke, possono contenere un elenco di stringhe di testo per integrare il contenuto video o audio. Queste stringhe di testo contengono metadati sul contenuto, ad esempio titoli di canzoni, nomi di artisti, informazioni sul genere e così via. Le stringhe di testo possono essere presenti in più di una lingua. Queste stringhe sono facoltative e molti dischi non sono disponibili.

Per recuperare le stringhe di testo da un DVD, usare l'interfaccia [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , esposta dal [navigatore DVD](dvd-navigator-filter.md). In realtà non è necessario creare un grafico di riproduzione DVD per recuperare le stringhe di testo. È sufficiente creare il navigatore DVD, impostare il volume DVD e quindi chiamare i metodi di stringa di testo pertinenti:



| Metodo                                                                                  | Descrizione                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | Ottiene il numero di lingue per cui sono presenti stringhe di testo.                                                                                                                                  |
| [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | Ottiene informazioni sulle stringhe di testo per una lingua.                                                                                                                                       |
| [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | Ottiene una stringa di testo per una lingua specificata, in base all'indice.                                                                                                                                          |
| [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | Ottiene una stringa di testo come matrice di byte non elaborata. Utilizzare questo metodo se la stringa di testo utilizza una codifica dei caratteri non supportata da [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode). |



 

Di seguito è riportata la procedura di base per ottenere le stringhe di testo:

1.  Chiamare [**IDvdInfo2:: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) per trovare il numero totale di lingue in cui vengono visualizzate le stringhe di testo. Se il numero è zero, significa che il DVD non contiene stringhe di testo. Questo è probabilmente il caso più comune, infatti.
2.  Se il numero di lingue è almeno uno, chiamare [**IDvdInfo2:: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) per ottenere informazioni su ogni lingua. Il linguaggio è specificato dall'indice. Il metodo restituisce il numero totale di stringhe di testo in tale lingua, l'identificatore delle impostazioni locali (**LCID**) per la lingua e la codifica dei caratteri (Unicode o other). Le stringhe di testo DVD possono usare diversi set di caratteri diversi. sono elencate in [**DVD \_ TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).
3.  Per ottenere una stringa di testo, chiamare [**IDvdInfo2:: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) o [**IDvdInfo2:: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative). Il primo metodo restituisce una stringa di caratteri wide, ma non supporta tutti i set di caratteri. Il secondo metodo restituisce una matrice di byte che contiene i dati di testo non elaborati. Per entrambi i metodi, è possibile chiamare il metodo con un puntatore del buffer **null** per trovare la dimensione della stringa e il tipo di testo. Quindi allocare un buffer e chiamare di nuovo il metodo per ottenere la stringa.

A ogni stringa di testo è associato un codice identificatore, che indica il significato della stringa di testo. L'identificatore viene restituito come valore [**\_ TextStringType DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) . Esistono due categorie di identificatore: *identificatori di struttura* e *identificatori di contenuto*. Gli identificatori di struttura hanno codici numerici nell'intervallo da 0x00 a 0x02F. Gli identificatori di contenuto hanno un intervallo di 0x30 e versioni successive. L'enumerazione **DVD \_ TextStringType** definisce un subset degli identificatori più comuni, ma i metodi [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) possono restituire qualsiasi codice identificatore. Un identificatore di struttura descrive una parte logica del DVD, ad esempio volume, titolo o parte del titolo (PTT). Un identificatore del contenuto indica il significato di una determinata stringa di testo, ad esempio titolo del film, titolo del brano o genere.

Agli identificatori di struttura non sono associate stringhe di testo. Quando un identificatore di struttura viene visualizzato nei dati della stringa di testo, segnala che le stringhe di testo seguenti si applicano alla parte logica del DVD, fino all'identificatore di struttura successivo. La posizione degli identificatori di struttura all'interno dei dati di testo corrisponde alla gerarchia logica del volume DVD. Ad esempio, la prima occorrenza dell' \_ identificatore del titolo della struct DVD \_ (0x02) rappresenta il primo titolo del volume e l'occorrenza successiva rappresenta il secondo titolo.

La tabella seguente illustra in che modo è possibile definire le stringhe di testo per un DVD con due titoli.



| \_TEXTSTRINGTYPE DVD        | Stringa di testo  | Descrizione                                    |
|----------------------------|--------------|------------------------------------------------|
| \_Volume struct DVD \_ (0x01) | ""           | Identificatore della struttura per l'intero lato del disco. |
| \_Nome generale DVD \_ (0x30)  | "Volume DVD" | Nome del volume DVD.                               |
| \_Titolo struct DVD \_ (0x02)  | ""           | Identificatore di struttura per il primo titolo.      |
| \_Nome generale DVD \_ (0x30)  | "Title 1"    | Nome del primo titolo.                       |
| \_Titolo struct DVD \_ (0x02)  | ""           | Identificatore di struttura per il secondo titolo.     |
| \_Nome generale DVD \_ (0x30)  | "Title 2"    | Nome del secondo titolo.                      |



 

I metodi [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) e [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) considerano gli identificatori di struttura e gli identificatori di contenuto uguali. L'unica differenza è che per gli identificatori di struttura il buffer di testo associato è vuoto. Spetta all'applicazione tenere traccia della relazione tra le stringhe di testo e le parti logiche del DVD.

Nell'esempio seguente viene illustrato come ottenere stringhe di testo da un DVD. Questo esempio Ignora alcuni dettagli necessari per un'applicazione reale. Ad esempio, ignora gli identificatori di struttura. L'esempio ha lo scopo di mostrare solo la sequenza di chiamate corretta.


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



Per informazioni sulle stringhe di testo DVD, vedere il [sito Web del forum](https://go.microsoft.com/fwlink/?LinkId=8677)relativo ai DVD.

Il metodo **CDvdCore:: GetDvdText** nell'applicazione DVDSample illustra i passaggi di base per l'enumerazione e la visualizzazione delle stringhe di testo DVD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



