---
description: Implementazione di IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementazione di IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304159"
---
# <a name="implementing-iamerrorlog"></a>Implementazione di IAMErrorLog

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

L'interfaccia [**IAMErrorLog**](iamerrorlog.md) contiene un solo metodo, [**LogError**](iamerrorlog-logerror.md). I parametri del metodo contengono informazioni sull'errore che si è verificato.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



Il codice di errore e la stringa di errore sono definiti da servizi di modifica DirectShow. Per un elenco di errori, vedere [errori di rendering](rendering-errors.md).

Il parametro *pExtraInfo* contiene un puntatore a un tipo Variant che contiene informazioni aggiuntive sull'errore. Il tipo di dati e il contenuto della variante variano a seconda dell'errore specifico che si è verificato. Se, ad esempio, l'errore è stato causato da un nome di file errato, VARIANT è una stringa con il nome file non valido. Alcuni errori non contengono informazioni aggiuntive, quindi *pExtraInfo* potrebbe essere **null**. Nel codice seguente viene illustrato come testare il membro **VT** della variante, che indica il tipo di dati e formattare un messaggio di conseguenza.


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
> Non liberare il VARIANT a cui punta
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
> . Inoltre, la variante diventa non valida dopo la restituzione del metodo, pertanto non è possibile farvi riferimento in un secondo momento.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



