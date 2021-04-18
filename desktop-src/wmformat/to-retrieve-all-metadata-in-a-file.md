---
title: Per recuperare tutti i metadati in un file
description: Per recuperare tutti i metadati in un file
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows Media Format SDK, recupero di metadati
- Formato di sistemi avanzati (ASF), recupero di metadati
- ASF (Advanced Systems Format), recupero di metadati
- metadati, recupero di tutti i
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc5d63a27cd4455d8d39cebee894dfbfc8d5bf2c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299397"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>Per recuperare tutti i metadati in un file

L'esempio di codice seguente è una funzione che Visualizza tutti i metadati in un file. Per usare la funzione, è necessario passare un puntatore all'interfaccia [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) di un oggetto editor di metadati, un oggetto Reader, un oggetto Reader sincrono o un oggetto writer. È inoltre necessario includere il file di intestazione stdio. h in un punto qualsiasi del progetto. Per ulteriori informazioni sull'utilizzo di questo esempio, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).

Per maggiore chiarezza, in questo esempio non vengono visualizzati i valori degli attributi Binary e GUID. Per gli attributi binari, è necessario verificare se il nome dell'attributo corrisponde a uno qualsiasi degli attributi di metadati complessi noti. In tal caso, è necessario formattare l'output in base alla struttura utilizzata per l'attributo. Analogamente, i valori degli attributi GUID possono essere visualizzati in diversi modi. È possibile scegliere di visualizzare ogni membro della struttura uno alla volta oppure convertire la struttura in una stringa e visualizzarla come un unico valore.


```C++
HRESULT ShowAllAttributes(IWMHeaderInfo3* pHeaderInfo)
{
    HRESULT hr          = S_OK;
    
    WORD    cAttributes = 0;
    WCHAR*  pwszName    = NULL;
    WORD    cchName     = 0;
    BYTE*   pbValue     = NULL;
    DWORD   cbValue     = 0;
    WORD    langIndex   = 0;
    WORD    attIndex    = 0;

    WMT_ATTR_DATATYPE attType;

    // Get the total number of attributes in the file.

    hr = pHeaderInfo->GetAttributeCountEx(0xFFFF, &cAttributes);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all the attributes, retrieving and displaying each.

    for(attIndex = 0; attIndex < cAttributes; attIndex++)
    {
        // Get the required buffer lengths for the name and value.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                NULL,
                                                &cchName,
                                                NULL,
                                                NULL,
                                                NULL,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate the buffers.

        pwszName = new WCHAR[cchName];
        if(pwszName == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        pbValue = new BYTE[cbValue];
        if(pbValue == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the attribute.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                pwszName,
                                                &cchName,
                                                &attType,
                                                &langIndex,
                                                pbValue,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Display the attribute global index and name.

        printf("%3d - %S (Language %d):\n\t ", attIndex, pwszName, langIndex);

        // Display the attribute depending upon type.

        switch(attType)
        {
        case WMT_TYPE_DWORD:
        case WMT_TYPE_QWORD:
        case WMT_TYPE_WORD:
            printf("%d\n\n", (DWORD) *pbValue);
            break;
        case WMT_TYPE_STRING:
            printf("%S\n\n", (WCHAR*) pbValue);
            break;
        case WMT_TYPE_BINARY:
            printf("<binary value>\n\n");
            break;
        case WMT_TYPE_BOOL:
            printf("%s\n\n", ((BOOL) *pbValue == TRUE) ? "True" : "False");
            break;
        case WMT_TYPE_GUID:
            printf("<GUID value>\n\n", (DWORD) *pbValue);
            break;
        }

        // Release allocated memory for the next pass.

        SAFE_ARRAY_DELETE(pwszName);
        SAFE_ARRAY_DELETE(pbValue);
        cchName = 0;
        cbValue = 0;
    } // End for attIndex.

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero degli attributi dei metadati**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




