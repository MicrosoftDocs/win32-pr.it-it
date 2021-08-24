---
title: Uso di attributi di metadati complessi
description: Uso di attributi di metadati complessi
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows MEDIA Format SDK, attributi di metadati complessi
- Advanced Systems Format (ASF), attributi di metadati complessi
- ASF (Advanced Systems Format), attributi di metadati complessi
- metadati, attributi complessi
- attributi di metadati complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8245d2fbc07878a73e304cfc573e05e93b605185ece93655dae7a8bdeff0d9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807251"
---
# <a name="using-complex-metadata-attributes"></a>Uso di attributi di metadati complessi

L Windows Media Format SDK supporta attributi di metadati complessi, ovvero attributi con valori rappresentati da una struttura . Poiché tutti gli attributi devono avere un tipo di dati definito nell'enumerazione [**WMT \_ ATTR \_ DATATYPE,**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) tutti gli attributi di metadati complessi vengono considerati **come WMT \_ TYPE \_ BINARY.** Quando si scrive un attributo complesso, eseguire il cast del puntatore alla struttura come puntatore di byte. Quando si recupera un attributo complesso, eseguire il cast della matrice di byte impostata da [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) come struttura appropriata.

Negli esempi di codice seguenti viene illustrato come impostare e recuperare un attributo di metadati complesso. La prima funzione aggiunge un attributo di testo utente, la seconda funzione ne recupera uno. Per altre informazioni su come usare questi esempi, vedere [Uso degli esempi di codice.](using-the-code-examples.md)


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




