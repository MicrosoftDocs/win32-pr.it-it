---
description: Implementazione di DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementazione di DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125037"
---
# <a name="implementing-dllregisterserver"></a>Implementazione di DllRegisterServer

Il passaggio finale consiste nell'implementare la funzione **DllRegisterServer** . La DLL che contiene il componente deve esportare questa funzione. La funzione verrà chiamata da un'applicazione di configurazione o quando l'utente esegue lo strumento Regsvr32.exe.

Nell'esempio seguente viene illustrata un'implementazione minima di **DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



La funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crea voci del registro di sistema per ogni componente nel


```
g_Templates
```



matrice. Questa funzione presenta tuttavia alcune limitazioni. Innanzitutto, assegna tutti i filtri alla categoria "DirectShow Filters" (CLSID \_ LegacyAmFilterCategory), ma non tutti i filtri appartengono a questa categoria. I filtri di acquisizione e di compressione, ad esempio, hanno categorie personalizzate. In secondo luogo, se il filtro supporta un dispositivo hardware, potrebbe essere necessario registrare due informazioni aggiuntive non gestite da **AMovieDLLRegisterServer2** , ovvero la categoria *media* e *pin*. Un supporto definisce un metodo di comunicazione in un dispositivo hardware, ad esempio un bus. La categoria pin definisce la funzione di un PIN. Per informazioni sui supporti, vedere "KSPIN \_ medium" in Microsoft Windows Driver Development Kit (DDK). Per un elenco di categorie di pin, vedere [impostare la proprietà pin](pin-property-set.md).

Se si desidera specificare una categoria di filtro, un supporto o una categoria di pin, chiamare il metodo [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) dall'interno di **DllRegisterServer**. Questo metodo accetta un puntatore a una struttura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , che specifica le informazioni sul filtro.

Per complicare un po' le cose, la struttura **REGFILTER2** supporta due formati diversi per la registrazione dei pin. Il membro **dwVersion** specifica il formato:

-   Se **dwVersion** è 1, il formato del PIN è **AMOVIESETUP \_ pin** (descritto in precedenza).
-   Se **dwVersion** è 2, il formato del PIN è [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).

La struttura **REGFILTERPINS2** include voci per supporti pin e categorie pin. USA anche i flag di bit per alcuni elementi che **AMOVIESETUP \_ pin** dichiara come valori booleani.

Nell'esempio seguente viene illustrato come chiamare **IFilterMapper2:: RegisterFilter** dall'interno di **DllRegisterServer**:


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



 

 



