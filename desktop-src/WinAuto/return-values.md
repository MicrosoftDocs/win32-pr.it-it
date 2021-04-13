---
title: Valori restituiti (funzionalità di accessibilità di Windows)
description: In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati con minore frequenza.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474771"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="13f10-103">Valori restituiti (funzionalità di accessibilità di Windows)</span><span class="sxs-lookup"><span data-stu-id="13f10-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="13f10-104">In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati con minore frequenza.</span><span class="sxs-lookup"><span data-stu-id="13f10-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="13f10-105">Valori restituiti comuni</span><span class="sxs-lookup"><span data-stu-id="13f10-105">Common Return Values</span></span>

<span data-ttu-id="13f10-106">I metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituiscono uno dei valori seguenti, definiti in Winerror. h, o un altro codice di errore Component Object Model standard (com):</span><span class="sxs-lookup"><span data-stu-id="13f10-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f10-107">\_OK</span><span class="sxs-lookup"><span data-stu-id="13f10-107">S\_OK</span></span>                   | <span data-ttu-id="13f10-108">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="13f10-108">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="13f10-109">S \_ false</span><span class="sxs-lookup"><span data-stu-id="13f10-109">S\_FALSE</span></span>                | <span data-ttu-id="13f10-110">Il metodo è riuscito in parte.</span><span class="sxs-lookup"><span data-stu-id="13f10-110">The method succeeded in part.</span></span> <span data-ttu-id="13f10-111">Questo errore si verifica quando il metodo ha esito positivo, ma le informazioni richieste non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="13f10-111">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="13f10-112">Ad esempio, Microsoft Active Accessibility restituisce \_ false se si chiama [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) per recuperare un oggetto figlio in un determinato punto e il punto specificato non si trova all'interno dell'oggetto o dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="13f10-112">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="13f10-113">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13f10-113">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="13f10-114">L'oggetto non supporta la proprietà o l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="13f10-114">The object does not support the requested property or action.</span></span> <span data-ttu-id="13f10-115">Un pulsante di push, ad esempio, restituisce questo valore se si richiede la relativa [proprietà Value](value-property.md), perché non dispone di una proprietà Value.</span><span class="sxs-lookup"><span data-stu-id="13f10-115">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="13f10-116">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="13f10-116">E\_NOTIMPL</span></span>              | <span data-ttu-id="13f10-117">Il metodo non è implementato.</span><span class="sxs-lookup"><span data-stu-id="13f10-117">The method is not implemented.</span></span> <span data-ttu-id="13f10-118">Questo valore si verifica quando un client chiama un metodo non ancora supportato in quel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="13f10-118">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="13f10-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13f10-119">E\_INVALIDARG</span></span>           | <span data-ttu-id="13f10-120">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="13f10-120">One or more arguments were not valid.</span></span> <span data-ttu-id="13f10-121">Questo errore si verifica quando il chiamante tenta di identificare un oggetto figlio utilizzando un identificatore non riconosciuto dal server.</span><span class="sxs-lookup"><span data-stu-id="13f10-121">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="13f10-122">Questo errore si verifica anche quando un client tenta di identificare un oggetto figlio all'interno di un oggetto privo di elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="13f10-122">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="13f10-123">E \_ OutOfMemory</span><span class="sxs-lookup"><span data-stu-id="13f10-123">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="13f10-124">Il metodo non è riuscito ad allocare la memoria necessaria per completare un'operazione cruciale per il suo esito positivo.</span><span class="sxs-lookup"><span data-stu-id="13f10-124">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="13f10-125">E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="13f10-125">E\_FAIL</span></span>                 | <span data-ttu-id="13f10-126">Si è verificato un errore sconosciuto o generico.</span><span class="sxs-lookup"><span data-stu-id="13f10-126">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="13f10-127">Valori restituiti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="13f10-127">Additional Return Values</span></span>

<span data-ttu-id="13f10-128">Di seguito sono riportati i valori restituiti che possono essere restituiti dai metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="13f10-128">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="13f10-129">Questi valori restituiti non sono comuni come quelli precedenti, ma è necessario conoscerli.</span><span class="sxs-lookup"><span data-stu-id="13f10-129">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="13f10-130">E \_ AccessDenied</span><span class="sxs-lookup"><span data-stu-id="13f10-130">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="13f10-131">Viene restituito quando si chiama Get \_ accValue per ottenere il valore di un controllo password.</span><span class="sxs-lookup"><span data-stu-id="13f10-131">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="13f10-132">\_eccezione disp E \_</span><span class="sxs-lookup"><span data-stu-id="13f10-132">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="13f10-133">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="13f10-133">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




