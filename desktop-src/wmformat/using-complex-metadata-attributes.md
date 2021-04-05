---
title: Uso di attributi di metadati complessi
description: Uso di attributi di metadati complessi
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows Media Format SDK, attributi di metadati complessi
- Advanced Systems Format (ASF), attributi di metadati complessi
- ASF (Advanced Systems Format), attributi di metadati complessi
- metadati, attributi complessi
- attributi di metadati complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd03c656a8cba5342d21e41932365455daa8bfa
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336337"
---
# <a name="using-complex-metadata-attributes"></a><span data-ttu-id="70db8-108">Uso di attributi di metadati complessi</span><span class="sxs-lookup"><span data-stu-id="70db8-108">Using Complex Metadata Attributes</span></span>

<span data-ttu-id="70db8-109">Windows Media Format SDK supporta attributi di metadati complessi, ovvero attributi con valori rappresentati da una struttura.</span><span class="sxs-lookup"><span data-stu-id="70db8-109">The Windows Media Format SDK supports complex metadata attributes, which are attributes that have values represented by a structure.</span></span> <span data-ttu-id="70db8-110">Poiché tutti gli attributi devono avere un tipo di dati definito nell'enumerazione [**WMT \_ attr \_ DataType**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) , tutti gli attributi di metadati complessi vengono considerati **\_ \_ binari di tipo WMT**.</span><span class="sxs-lookup"><span data-stu-id="70db8-110">Because all attributes must have a data type defined in the [**WMT\_ATTR\_DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) enumeration, all complex metadata attributes are treated as **WMT\_TYPE\_BINARY**.</span></span> <span data-ttu-id="70db8-111">Quando si scrive un attributo complesso, eseguire il cast del puntatore alla struttura come puntatore di byte.</span><span class="sxs-lookup"><span data-stu-id="70db8-111">When writing a complex attribute, cast the pointer to the structure as a byte pointer.</span></span> <span data-ttu-id="70db8-112">Quando si recupera un attributo complesso, eseguire il cast della matrice di byte impostata da [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) come struttura appropriata.</span><span class="sxs-lookup"><span data-stu-id="70db8-112">When you retrieve a complex attribute, cast the array of bytes set by [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) as the appropriate structure.</span></span>

<span data-ttu-id="70db8-113">Negli esempi di codice seguenti viene illustrato come impostare e recuperare un attributo di metadati complessi.</span><span class="sxs-lookup"><span data-stu-id="70db8-113">The following code examples show how to set and retrieve a complex metadata attribute.</span></span> <span data-ttu-id="70db8-114">La prima funzione aggiunge un attributo di testo utente, la seconda funzione ne recupera una.</span><span class="sxs-lookup"><span data-stu-id="70db8-114">The first function adds a user text attribute, the second function retrieves one.</span></span> <span data-ttu-id="70db8-115">Per ulteriori informazioni sull'utilizzo di questi esempi, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="70db8-115">For more information about how to use these examples, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="70db8-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70db8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70db8-117">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="70db8-117">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




