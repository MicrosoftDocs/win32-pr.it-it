---
description: Implementazione di IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementazione di IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de0ab694b2e2b8868717b6b4c11b2124ecc4042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982204"
---
# <a name="implementing-iamerrorlog"></a>Implementazione di IAMErrorLog

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

[**L'interfaccia IAMErrorLog**](iamerrorlog.md) contiene un singolo metodo, [**LogError.**](iamerrorlog-logerror.md) I parametri del metodo contengono informazioni sull'errore che si è verificato.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



Il codice di errore e la stringa di errore sono definiti DirectShow Servizi di modifica. Per un elenco degli errori, vedere [Errori di rendering.](rendering-errors.md)

Il *parametro pExtraInfo* contiene un puntatore a un tipo VARIANT che contiene informazioni aggiuntive sull'errore. Il tipo di dati e il contenuto di VARIANT dipendono dall'errore specifico che si è verificato. Ad esempio, se l'errore è stato causato da un nome di file non corretto, VARIANT è una stringa con il nome file non valido. Alcuni errori non hanno informazioni aggiuntive, quindi *pExtraInfo* potrebbe essere **NULL.** Il codice seguente illustra come testare il **membro vt** di VARIANT, che indica il tipo di dati, e formattare un messaggio di conseguenza.


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
> 
>
> 
| Etichetta | Valore |
|--------|-------|
| <pre><code>pExtraInfo</code></pre> | 

>
> 
>
> . Inoltre, variant diventa non valido dopo la fine del metodo, quindi non fare riferimento a esso in un secondo momento.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



