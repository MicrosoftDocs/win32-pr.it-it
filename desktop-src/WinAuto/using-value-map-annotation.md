---
title: Uso dell'annotazione della mappa di valori
description: Per il codice di esempio, vedere esempio di annotazione della mappa dei valori.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399080"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="b8bf6-103">Uso dell'annotazione della mappa di valori</span><span class="sxs-lookup"><span data-stu-id="b8bf6-103">Using Value Map Annotation</span></span>

<span data-ttu-id="b8bf6-104">**Per creare una mappa di valori**</span><span class="sxs-lookup"><span data-stu-id="b8bf6-104">**To create a value map**</span></span>

1.  <span data-ttu-id="b8bf6-105">**Creare una stringa di mapping.**</span><span class="sxs-lookup"><span data-stu-id="b8bf6-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="b8bf6-106">Una stringa di mapping è un elenco di valori numerici di un controllo corrispondenti a una stringa leggibile in Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="b8bf6-107">Inizia con "A:" seguito da un numero che indica il tipo di indice usato.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="b8bf6-108">Sono supportati solo gli indici di immagini; Pertanto, il tipo di indice è sempre 0.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="b8bf6-109">La stringa è seguita da coppie index: result.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="b8bf6-110">"Index" è un numero che rappresenta un indice di immagine per un List-View o una visualizzazione ad albero oppure il valore per un controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="b8bf6-111">Il valore risultante è un numero ottenuto quando si esegue il mapping della proprietà Role o state per una visualizzazione elenco o un controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="b8bf6-112">Tali numeri sono espressi in formato decimale o esadecimale con prefisso "0x".</span><span class="sxs-lookup"><span data-stu-id="b8bf6-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="b8bf6-113">La stringa di mapping viene sempre terminata con i due punti finali (":").</span><span class="sxs-lookup"><span data-stu-id="b8bf6-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="b8bf6-114">Di seguito è riportato un esempio di mapping delle annotazioni per le proprietà state e Role di una casella di controllo in una visualizzazione elenco o in un controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="b8bf6-115">Nella vista sono presenti due elementi che rappresentano le caselle di controllo e ognuna contiene immagini corrispondenti allo stato selezionato e non selezionato.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="b8bf6-116">Per i valori di ruolo e stato validi, vedere la pagina relativa ai [ruoli oggetto](object-roles.md) e alle [costanti di stato dell'oggetto](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8bf6-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="b8bf6-117">Il valore di indice può essere negativo quando si esegue il mapping delle proprietà per un controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="b8bf6-118">Quando si esegue il mapping di una proprietà Value o Description, il risultato è una stringa.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="b8bf6-119">Le stringhe non sono racchiuse tra virgolette e i due punti fungono da delimitatori.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="b8bf6-120">Per altre informazioni, vedere [formato della mappa delle annotazioni](value-map-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="b8bf6-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="b8bf6-121">**Creare il gestore di annotazioni e ottenere un puntatore alla relativa** interfaccia [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**</span><span class="sxs-lookup"><span data-stu-id="b8bf6-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="b8bf6-122">Di seguito è riportato un esempio di come creare il gestore di annotazioni.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="b8bf6-123">**Alleghi la stringa di mapping al controllo.**</span><span class="sxs-lookup"><span data-stu-id="b8bf6-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="b8bf6-124">Chiamare [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passando l' **HWND** del controllo e un puntatore alla stringa di mapping.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="b8bf6-125">Il parametro *IdProp* sarà uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="b8bf6-126">Parametro</span><span class="sxs-lookup"><span data-stu-id="b8bf6-126">Parameter</span></span>                   | <span data-ttu-id="b8bf6-127">Usato per</span><span class="sxs-lookup"><span data-stu-id="b8bf6-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="b8bf6-128">\_ROLEMAP MSAAPROPID</span><span class="sxs-lookup"><span data-stu-id="b8bf6-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="b8bf6-129">Per impostare una mappa dei ruoli per i controlli visualizzazione elenco o visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="b8bf6-130">\_STATEMAP MSAAPROPID</span><span class="sxs-lookup"><span data-stu-id="b8bf6-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="b8bf6-131">Per impostare una mappa di stato per i controlli visualizzazione elenco o visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="b8bf6-132">\_DESCRIPTIONMAP ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="b8bf6-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="b8bf6-133">Per impostare una mappa di descrizione per la visualizzazione elenco o le visualizzazioni albero.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="b8bf6-134">\_VALUEMAP MSAAPROPID</span><span class="sxs-lookup"><span data-stu-id="b8bf6-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="b8bf6-135">Per impostare una mappa di valori nei controlli dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="b8bf6-136">**Pulisci.**</span><span class="sxs-lookup"><span data-stu-id="b8bf6-136">**Clean up.**</span></span>

    <span data-ttu-id="b8bf6-137">Prima di eliminare i controlli con annotazioni della mappa dei valori (ad esempio, quando si gestisce la [ \_ distruzione WM](../winmsg/wm-destroy.md)), è necessario deselezionare le proprietà precedentemente registrate e rilasciare il gestore di annotazioni.</span><span class="sxs-lookup"><span data-stu-id="b8bf6-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="b8bf6-138">A tale scopo, chiamare [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) in base alle esigenze e rilasciare il puntatore su [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span><span class="sxs-lookup"><span data-stu-id="b8bf6-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="b8bf6-139">Per il codice di esempio, vedere [esempio di annotazione della mappa dei valori](value-map-annotation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b8bf6-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 