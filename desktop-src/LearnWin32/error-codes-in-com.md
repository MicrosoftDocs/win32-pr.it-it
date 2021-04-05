---
title: Codici di errore in COM
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725386"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="ee25b-103">Codici di errore in COM</span><span class="sxs-lookup"><span data-stu-id="ee25b-103">Error Codes in COM</span></span>

<span data-ttu-id="ee25b-104">Per indicare l'esito positivo o negativo, i metodi e le funzioni COM restituiscono un valore di tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ee25b-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="ee25b-105">**HRESULT** è un valore integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ee25b-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="ee25b-106">Il bit più significativo del valore **HRESULT** segnala l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ee25b-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="ee25b-107">Zero (0) indica esito positivo e 1 indica un errore.</span><span class="sxs-lookup"><span data-stu-id="ee25b-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="ee25b-108">Producendo gli intervalli numerici seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee25b-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="ee25b-109">Codici di esito positivo: 0x0 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ee25b-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="ee25b-110">Codici di errore: 0x80000000 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ee25b-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="ee25b-111">Un numero ridotto di metodi COM non restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee25b-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="ee25b-112">Ad esempio, i metodi [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) restituiscono valori long senza segno.</span><span class="sxs-lookup"><span data-stu-id="ee25b-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="ee25b-113">Tuttavia, ogni metodo COM che restituisce un codice di errore esegue questa operazione restituendo un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee25b-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="ee25b-114">Per controllare se un metodo COM ha esito positivo, esaminare il bit più significativo dell' **HRESULT** restituito.</span><span class="sxs-lookup"><span data-stu-id="ee25b-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="ee25b-115">Le intestazioni Windows SDK forniscono due macro che semplificano questa operazione, ovvero la macro [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) e la macro [**non riuscita**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="ee25b-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="ee25b-116">La macro **succeeded** restituisce **true** se un **HRESULT** è un codice di esito positivo e **false** se è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ee25b-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="ee25b-117">Nell'esempio seguente viene verificato se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ee25b-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="ee25b-118">A volte è più pratico testare la condizione inversa.</span><span class="sxs-lookup"><span data-stu-id="ee25b-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="ee25b-119">La macro non [**riuscita**](/windows/desktop/api/winerror/nf-winerror-failed) esegue l'operazione opposta rispetto a [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span><span class="sxs-lookup"><span data-stu-id="ee25b-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="ee25b-120">Restituisce **true** per un codice di errore e **false** per un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ee25b-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="ee25b-121">Più avanti in questo modulo, si esamineranno alcuni consigli pratici su come strutturare il codice per gestire gli errori COM.</span><span class="sxs-lookup"><span data-stu-id="ee25b-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="ee25b-122">Vedere [gestione degli errori in com](error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="ee25b-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="ee25b-123">Prossima</span><span class="sxs-lookup"><span data-stu-id="ee25b-123">Next</span></span>

[<span data-ttu-id="ee25b-124">Creazione di un oggetto in COM</span><span class="sxs-lookup"><span data-stu-id="ee25b-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 