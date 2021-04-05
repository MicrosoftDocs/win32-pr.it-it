---
title: Uso dei marcatori
description: Uso dei marcatori
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marcatori
- Advanced Systems Format (ASF), marcatori
- ASF (formato avanzato dei sistemi), marcatori
- Formato di sistemi avanzati (ASF), ricerca di marcatori
- ASF (formato avanzato dei sistemi), ricerca di marcatori
- marcatori, informazioni
- marcatori, aggiunta
- marcatori, rimozione
- marcatori, recupero
- marcatori, ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724116"
---
# <a name="using-markers"></a>Uso dei marcatori

Un *marcatore* è un punto denominato all'interno di un file ASF. Ogni marcatore è costituito da un nome e da un orario associato, misurato come offset dall'inizio del file. Un'applicazione può usare i marcatori per assegnare nomi a diversi punti all'interno del contenuto, visualizzare i nomi dell'utente e quindi cercare le posizioni del marcatore. Un'applicazione può aggiungere o rimuovere marcatori da un file ASF esistente.

L'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contiene i metodi per lavorare con i marcatori. L'oggetto dell'editor di metadati supporta l'aggiunta e la rimozione di marcatori. Gli oggetti writer e Reader possono recuperare i marcatori ma non possono aggiungere o rimuovere marcatori.

## <a name="adding-markers"></a>Aggiunta di marcatori

Per aggiungere un marcatore, eseguire una query sull'editor dei metadati per l'interfaccia **IWMHeaderInfo** . Chiamare quindi il metodo [**IWMHeaderInfo:: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , specificando il nome del marcatore come stringa di caratteri wide e l'ora in unità 100-nanosecondi. Il tempo non deve superare la durata del file. Due marcatori possono avere la stessa ora.

Nell'esempio seguente vengono aggiunti diversi marcatori a un file:


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>Rimozione di marcatori

Per rimuovere un marcatore, chiamare [**IWMHeaderInfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specificando l'indice del marcatore da rimuovere. I marcatori vengono ordinati automaticamente in ordine di tempo crescente, pertanto l'indice 0 è sempre il primo marcatore. Si noti che la chiamata a **RemoveMarker** modifica i numeri di indice di tutti i marcatori che seguono. Il codice seguente, in cui *pInfo* è un puntatore a un'interfaccia **IWMHeaderInfo** , rimuove tutti i marcatori da un file:


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>Recupero di marcatori

Per recuperare il nome e l'ora di un marcatore, seguire questa procedura:

1.  Chiamare il metodo [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) per determinare il numero di marcatori contenuti nel file.
2.  Recuperare le dimensioni della stringa necessaria per contenere il nome del marcatore. A tale scopo, chiamare il metodo [**IWMHeaderInfo:: Getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) . Specificare l'indice del marcatore da recuperare e **null** per il buffer di stringa (il parametro *pwszMarkerName* ). Il metodo restituisce la lunghezza della stringa, incluso il carattere di terminazione ' \\ 0', nel parametro *pcchMarkerNameLen* .
3.  Allocare una stringa di caratteri wide per ricevere il nome.
4.  Chiamare nuovamente **Getmarker** , ma questa volta passare l'indirizzo della stringa nel parametro *pwszMarkerName* . Il metodo scrive il nome del marcatore nella stringa e restituisce l'ora del marcatore nel parametro *pcnsMarkerTime* .

Il codice seguente esegue il ciclo di ogni marcatore in ordine e recupera il nome e l'ora:


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>Ricerca di un marcatore

Per avviare la riproduzione da una posizione del marcatore, chiamare il metodo [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) dell'oggetto Reader, specificando l'indice del marcatore. I parametri rimanenti sono identici a quelli per il metodo [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . Nell'esempio seguente viene eseguita una query sul Reader per l'interfaccia [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) e viene eseguita la ricerca del primo marcatore.


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




