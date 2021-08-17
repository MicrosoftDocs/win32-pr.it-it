---
description: Implementazione di DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementazione di DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39d55b73dd70a21c10df26a100f964917a57dd9f036ebd5c2708359bca1dd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998092"
---
# <a name="implementing-dllregisterserver"></a>Implementazione di DllRegisterServer

Il passaggio finale consiste nell'implementare la **funzione DllRegisterServer.** La DLL che contiene il componente deve esportare questa funzione. La funzione verrà chiamata da un'applicazione di configurazione o quando l'utente esegue lo Regsvr32.exe comando.

L'esempio seguente illustra un'implementazione minima **di DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



La [**funzione AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crea voci del Registro di sistema per ogni componente in


```
g_Templates
```



matrice. Tuttavia, questa funzione presenta alcune limitazioni. In primo luogo, assegna ogni filtro alla categoria "filtri DirectShow" (CLSID LegacyAmFilterCategory), ma non tutti i filtri appartengono \_ a questa categoria. I filtri di acquisizione e i filtri di compressione, ad esempio, hanno le proprie categorie. In secondo piano, se il filtro supporta un dispositivo hardware, potrebbe essere necessario registrare due informazioni aggiuntive  che **AMovieDLLRegisterServer2** non gestisce: il supporto e la categoria *pin*. Un supporto definisce un metodo di comunicazione in un dispositivo hardware, ad esempio un bus. La categoria pin definisce la funzione di un segnaposto. Per informazioni sui medium, vedere "KSPIN \_ MEDIUM" in Microsoft Windows Driver Development Kit (DDK). Per un elenco di categorie di pin, vedere [Aggiungere un set di proprietà.](pin-property-set.md)

Per specificare una categoria di filtro, un supporto o una categoria pin, chiamare il metodo [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) dall'interno di **DllRegisterServer**. Questo metodo accetta un puntatore a [**una struttura REGFILTER2,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) che specifica le informazioni sul filtro.

A complicare le cose, la **struttura REGFILTER2** supporta due formati diversi per la registrazione dei pin. Il **membro dwVersion** specifica il formato:

-   Se **dwVersion** è 1, il formato del pin è **IL \_ PIN AMOVIESETUP** (descritto in precedenza).
-   Se **dwVersion** è 2, il formato del pin è [**REGFILTERPINS2.**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2)

La **struttura REGFILTERPINS2** include voci per i medi di aggiunta e le categorie di pin. Usa inoltre flag di bit per alcuni elementi dichiarati **\_ dal PIN AMOVIESETUP** come valori booleani.

L'esempio seguente illustra come chiamare **IFilterMapper2::RegisterFilter** dall'interno **di DllRegisterServer**:


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



