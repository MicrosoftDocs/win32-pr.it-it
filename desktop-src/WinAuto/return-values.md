---
title: Valori restituiti (funzionalità di accessibilità di Windows)
description: In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati meno frequentemente.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443992"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="8df5b-103">Valori restituiti (funzionalità di accessibilità di Windows)</span><span class="sxs-lookup"><span data-stu-id="8df5b-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="8df5b-104">In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati meno frequentemente.</span><span class="sxs-lookup"><span data-stu-id="8df5b-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="8df5b-105">Valori restituiti comuni</span><span class="sxs-lookup"><span data-stu-id="8df5b-105">Common Return Values</span></span>

<span data-ttu-id="8df5b-106">I [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituiscono uno dei valori seguenti, definiti in winerror.h, o un altro codice di errore Component Object Model (COM) standard:</span><span class="sxs-lookup"><span data-stu-id="8df5b-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|   <span data-ttu-id="8df5b-107">Valore</span><span class="sxs-lookup"><span data-stu-id="8df5b-107">Value</span></span>                      |   <span data-ttu-id="8df5b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8df5b-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df5b-109">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="8df5b-109">S\_OK</span></span>                   | <span data-ttu-id="8df5b-110">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8df5b-110">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8df5b-111">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="8df5b-111">S\_FALSE</span></span>                | <span data-ttu-id="8df5b-112">Il metodo ha avuto esito positivo in parte.</span><span class="sxs-lookup"><span data-stu-id="8df5b-112">The method succeeded in part.</span></span> <span data-ttu-id="8df5b-113">Ciò si verifica quando il metodo ha esito positivo, ma le informazioni richieste non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="8df5b-113">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="8df5b-114">Ad esempio, Microsoft Active Accessibility restituisce S FALSE se si chiama \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) per recuperare un oggetto figlio in un determinato punto e il punto specificato non si trova all'interno dell'oggetto o dell'oggetto figlio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8df5b-114">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="8df5b-115">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8df5b-115">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="8df5b-116">L'oggetto non supporta la proprietà o l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8df5b-116">The object does not support the requested property or action.</span></span> <span data-ttu-id="8df5b-117">Ad esempio, un pulsante di comando restituisce questo valore se si richiede la proprietà [Value](value-property.md), perché non dispone di una proprietà Value.</span><span class="sxs-lookup"><span data-stu-id="8df5b-117">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="8df5b-118">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="8df5b-118">E\_NOTIMPL</span></span>              | <span data-ttu-id="8df5b-119">Il metodo non è implementato.</span><span class="sxs-lookup"><span data-stu-id="8df5b-119">The method is not implemented.</span></span> <span data-ttu-id="8df5b-120">Questo valore si verifica quando un client chiama un metodo non ancora supportato in tale sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8df5b-120">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8df5b-121">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8df5b-121">E\_INVALIDARG</span></span>           | <span data-ttu-id="8df5b-122">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="8df5b-122">One or more arguments were not valid.</span></span> <span data-ttu-id="8df5b-123">Questo errore si verifica quando il chiamante tenta di identificare un oggetto figlio utilizzando un identificatore non riconosciuto dal server.</span><span class="sxs-lookup"><span data-stu-id="8df5b-123">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="8df5b-124">Questo errore si verifica anche quando un client tenta di identificare un oggetto figlio all'interno di un oggetto senza elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="8df5b-124">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="8df5b-125">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8df5b-125">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="8df5b-126">Il metodo non è stato in grado di allocare la memoria necessaria per completare un'operazione fondamentale per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8df5b-126">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8df5b-127">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="8df5b-127">E\_FAIL</span></span>                 | <span data-ttu-id="8df5b-128">Si è verificato un errore sconosciuto o generico.</span><span class="sxs-lookup"><span data-stu-id="8df5b-128">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="8df5b-129">Valori restituiti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="8df5b-129">Additional Return Values</span></span>

<span data-ttu-id="8df5b-130">Di seguito sono riportati i valori [**restituiti che i metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) potrebbero restituire.</span><span class="sxs-lookup"><span data-stu-id="8df5b-130">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="8df5b-131">Questi valori restituiti non sono comuni come quelli precedenti, ma è necessario conoscerli.</span><span class="sxs-lookup"><span data-stu-id="8df5b-131">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|    <span data-ttu-id="8df5b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8df5b-132">Value</span></span>                    |    <span data-ttu-id="8df5b-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8df5b-133">Description</span></span>                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8df5b-134">E \_ ACCESSO NEGATO</span><span class="sxs-lookup"><span data-stu-id="8df5b-134">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="8df5b-135">Viene restituito quando si chiama get \_ accValue per ottenere il valore di un controllo password.</span><span class="sxs-lookup"><span data-stu-id="8df5b-135">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="8df5b-136">ECCEZIONE DISP \_ E \_</span><span class="sxs-lookup"><span data-stu-id="8df5b-136">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="8df5b-137">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="8df5b-137">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




