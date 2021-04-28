---
title: Codici di errore in COM
description: Codici di errore in COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103959"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="a48bc-103">Codici di errore in COM</span><span class="sxs-lookup"><span data-stu-id="a48bc-103">Error Codes in COM</span></span>

<span data-ttu-id="a48bc-104">Per indicare l'esito positivo o negativo, i metodi e le funzioni COM restituiscono un valore di tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a48bc-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="a48bc-105">HRESULT **è** un intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a48bc-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="a48bc-106">Il bit di ordine elevato di **HRESULT** segnala l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="a48bc-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="a48bc-107">Zero (0) indica l'esito positivo e 1 indica un errore.</span><span class="sxs-lookup"><span data-stu-id="a48bc-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="a48bc-108">In questo modo vengono prodotti gli intervalli numerici seguenti:</span><span class="sxs-lookup"><span data-stu-id="a48bc-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="a48bc-109">Codici di esito positivo: 0x0-0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a48bc-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="a48bc-110">Codici di errore: 0x80000000-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a48bc-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="a48bc-111">Un numero ridotto di metodi COM non restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a48bc-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="a48bc-112">Ad esempio, i [**metodi AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**e Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) restituiscono valori long senza segno.</span><span class="sxs-lookup"><span data-stu-id="a48bc-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="a48bc-113">Tuttavia, ogni metodo COM che restituisce un codice di errore restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a48bc-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="a48bc-114">Per verificare se un metodo COM ha esito positivo, esaminare il bit più alto **dell'HRESULT restituito.**</span><span class="sxs-lookup"><span data-stu-id="a48bc-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="a48bc-115">Le Windows SDK le intestazioni forniscono due macro che semplificano questa operazione: la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) e la macro [**FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed)</span><span class="sxs-lookup"><span data-stu-id="a48bc-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="a48bc-116">La macro **SUCCEEDED** restituisce **TRUE se** **un HRESULT** è un codice di esito positivo e **FALSE** se si tratta di un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a48bc-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="a48bc-117">Nell'esempio seguente viene verificato se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a48bc-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


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



<span data-ttu-id="a48bc-118">A volte è più comodo testare la condizione inversa.</span><span class="sxs-lookup"><span data-stu-id="a48bc-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="a48bc-119">La macro [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) esegue l'operazione opposta a [**SUCCEEDED.**](/windows/desktop/api/winerror/nf-winerror-succeeded)</span><span class="sxs-lookup"><span data-stu-id="a48bc-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="a48bc-120">Restituisce **TRUE per** un codice di errore e **FALSE per** un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a48bc-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


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



<span data-ttu-id="a48bc-121">Più avanti in questo modulo verranno visualizzati alcuni consigli pratici su come strutturare il codice per gestire gli errori COM.</span><span class="sxs-lookup"><span data-stu-id="a48bc-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="a48bc-122">Vedere [Gestione degli errori in COM.](error-handling-in-com.md)</span><span class="sxs-lookup"><span data-stu-id="a48bc-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="a48bc-123">Prossima</span><span class="sxs-lookup"><span data-stu-id="a48bc-123">Next</span></span>

[<span data-ttu-id="a48bc-124">Creazione di un oggetto in COM</span><span class="sxs-lookup"><span data-stu-id="a48bc-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 
