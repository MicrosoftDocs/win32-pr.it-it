---
description: Implementazione di IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementazione di IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446e193a6a28fc1cbd5515414b9914f2653e8bc27bb9b5a57e69d05dfc947d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398081"
---
# <a name="implementing-iamerrorlog"></a>Implementazione di IAMErrorLog

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

[**L'interfaccia IAMErrorLog**](iamerrorlog.md) contiene un singolo metodo, [**LogError**](iamerrorlog-logerror.md). I parametri del metodo contengono informazioni sull'errore che si è verificato.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



Il codice di errore e la stringa di errore sono definiti DirectShow Servizi di modifica. Per un elenco di errori, vedere [Errori di rendering](rendering-errors.md).

Il *parametro pExtraInfo* contiene un puntatore a un tipo VARIANT che contiene informazioni aggiuntive sull'errore. Il tipo di dati e il contenuto di VARIANT dipendono dall'errore specifico che si è verificato. Ad esempio, se l'errore è stato causato da un nome di file non corretto, VARIANT è una stringa con il nome file non valido. Alcuni errori non hanno informazioni aggiuntive, pertanto *pExtraInfo* potrebbe essere **NULL.** Il codice seguente illustra come testare il membro **vt** di VARIANT, che indica il tipo di dati, e formattare un messaggio di conseguenza.


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> Non liberare l'oggetto VARIANT a cui punta
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> . Inoltre, VARIANT diventa non valido dopo la fine del metodo, quindi non fare riferimento a esso in un secondo momento.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



