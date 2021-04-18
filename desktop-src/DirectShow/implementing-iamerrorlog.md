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
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="882c1-103">Implementazione di IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="882c1-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="882c1-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="882c1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="882c1-105">L'interfaccia [**IAMErrorLog**](iamerrorlog.md) contiene un solo metodo, [**LogError**](iamerrorlog-logerror.md).</span><span class="sxs-lookup"><span data-stu-id="882c1-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="882c1-106">I parametri del metodo contengono informazioni sull'errore che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="882c1-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="882c1-107">Il codice di errore e la stringa di errore sono definiti da servizi di modifica DirectShow.</span><span class="sxs-lookup"><span data-stu-id="882c1-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="882c1-108">Per un elenco di errori, vedere [errori di rendering](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="882c1-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="882c1-109">Il parametro *pExtraInfo* contiene un puntatore a un tipo Variant che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="882c1-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="882c1-110">Il tipo di dati e il contenuto della variante variano a seconda dell'errore specifico che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="882c1-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="882c1-111">Se, ad esempio, l'errore è stato causato da un nome di file errato, VARIANT è una stringa con il nome file non valido.</span><span class="sxs-lookup"><span data-stu-id="882c1-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="882c1-112">Alcuni errori non contengono informazioni aggiuntive, quindi *pExtraInfo* potrebbe essere **null**.</span><span class="sxs-lookup"><span data-stu-id="882c1-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="882c1-113">Nel codice seguente viene illustrato come testare il membro **VT** della variante, che indica il tipo di dati e formattare un messaggio di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="882c1-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


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
> <span data-ttu-id="882c1-114">Non liberare il VARIANT a cui punta</span><span class="sxs-lookup"><span data-stu-id="882c1-114">Do not free the VARIANT pointed to by</span></span>
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
> <span data-ttu-id="882c1-115">.</span><span class="sxs-lookup"><span data-stu-id="882c1-115">.</span></span> <span data-ttu-id="882c1-116">Inoltre, la variante diventa non valida dopo la restituzione del metodo, pertanto non è possibile farvi riferimento in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="882c1-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="882c1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="882c1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="882c1-118">Errori di registrazione</span><span class="sxs-lookup"><span data-stu-id="882c1-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



