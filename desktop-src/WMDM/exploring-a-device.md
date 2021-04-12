---
title: Esplorazione di un dispositivo
description: Esplorazione di un dispositivo
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Gestione dispositivi, esplorazione di dispositivi
- Gestione dispositivi, esplorazione dei dispositivi
- Guida per programmatori, esplorazione di dispositivi
- applicazioni desktop, esplorazione di dispositivi
- creazione di applicazioni Windows Media Gestione dispositivi, esplorazione di dispositivi
- esplorazione dei dispositivi
- depositi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396062"
---
# <a name="exploring-a-device"></a>Esplorazione di un dispositivo

L'esplorazione di un dispositivo è simile all'esplorazione di un'unità disco. Tutti gli oggetti in un dispositivo sono detti *archiviazione*. Una risorsa di archiviazione può essere un file, una cartella o un oggetto astratto (ad esempio una playlist) nel dispositivo. Per comprendere il tipo di archiviazione, è necessario esaminare gli attributi e i metadati di archiviazione (se supportati). Le archiviazioni sono organizzate gerarchicamente sul dispositivo. ogni risorsa di archiviazione ha esattamente un elemento padre e tutte le archiviazioni derivano da una singola risorsa di archiviazione del dispositivo radice, in genere denominata " \\ ".

I passaggi seguenti descrivono come esplorare un dispositivo:

1.  Ottenere l'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) di un dispositivo come descritto in [enumerazione dei dispositivi](enumerating-devices.md).
2.  Chiamare [**IWMDMDevice:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) per recuperare un'interfaccia [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) . Questa interfaccia viene usata per ottenere tutti gli oggetti figlio dell'archiviazione che restituisce questa interfaccia. Quando si recupera questa interfaccia dal dispositivo, come in questo caso, verrà mantenuta solo una risorsa di archiviazione: l'archiviazione del dispositivo radice.
3.  Chiamare [**IWMDMEnumStorage:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) con il conteggio 1 per recuperare l'interfaccia [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) per l'archiviazione del dispositivo radice. Non è possibile richiedere più di un elemento figlio dal dispositivo.
4.  Esaminare tutte le archiviazioni sul dispositivo richiamando in modo ricorsivo [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) e quindi **IWMDMEnumStorage:: Next** per ottenere gli elementi figlio di una risorsa di archiviazione. Per verificare se una risorsa di archiviazione dispone di elementi figlio per evitare le chiamate a **EnumStorage** e **Next**, è possibile chiamare [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) per verificare se i flag WMDM \_ storage \_ attr \_ contiene \_ files o WMDM \_ storage \_ attr \_ has \_ Folders. Per ulteriori informazioni su come ottenere le proprietà di una risorsa di archiviazione, vedere [ottenere e impostare metadati e attributi](getting-and-setting-metadata-and-attributes.md) e [ottenere e impostare metadati e attributi nell'applicazione](getting-and-setting-metadata-and-attributes-in-the-application.md).

Windows Media Gestione dispositivi non espone un set di cartelle standard per contenere supporti di un tipo specifico, ad esempio una cartella "playlist personali" per le playlist. Ogni dispositivo ha un file system univoco ed è necessario decidere in quale posizione è opportuno cercare o inviare un file specifico.

> [!Note]  
> Esplora risorse consente di visualizzare le cartelle virtuali che non esistono effettivamente nel dispositivo. Le cartelle virtuali di esempio sono le cartelle "supporti" e "dati" visualizzate per i dispositivi MTP. Queste cartelle vengono create da Windows per rendere più semplici i download per gli utenti finali; non esistono effettivamente nel dispositivo. L'applicazione non deve dipendere dalla ricerca di questi tipi di cartelle generali. Viceversa, Esplora risorse potrebbe non visualizzare alcune cartelle o oggetti che esistono nel dispositivo (ad esempio, playlist).

 

Nell'esempio di codice C++ riportato di seguito viene illustrata l'esplorazione ricorsiva di un dispositivo. USA due funzioni:

-   ExploreDevice, una funzione iniziale che riceve un puntatore di dispositivo e ottiene un puntatore all'enumeratore radice per quel dispositivo.
-   RecursiveExploreStorage, che viene chiamato per esplorare un dispositivo in modo ricorsivo.


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




