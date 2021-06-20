---
description: Implementare una pagina delle proprietà come parte della creazione di una pagina delle proprietà di filtro per un filtro DirectShow personalizzato.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Passaggio 4. Creare la pagina delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406854"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="e4ce0-104">Passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-104">Step 4.</span></span> <span data-ttu-id="e4ce0-105">Creare la pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="e4ce0-105">Create the Property Page</span></span>

<span data-ttu-id="e4ce0-106">A questo punto il filtro supporta tutti gli elementi di cui ha bisogno per una pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="e4ce0-107">Il passaggio successivo consiste nell'implementazione della pagina delle proprietà stessa.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="e4ce0-108">Per iniziare, derivare una nuova classe da **CBasePropertyPage**.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="e4ce0-109">L'esempio seguente illustra parte della dichiarazione, incluse alcune variabili membro private che verranno usate più avanti nell'esempio:</span><span class="sxs-lookup"><span data-stu-id="e4ce0-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="e4ce0-110">Creare quindi una risorsa finestra di dialogo nell'editor di risorse, insieme a una risorsa stringa per il titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="e4ce0-111">La stringa verrà visualizzata nella scheda della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="e4ce0-112">I due ID risorsa sono argomenti per il **costruttore CBasePropertyPage:**</span><span class="sxs-lookup"><span data-stu-id="e4ce0-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="e4ce0-113">La figura seguente mostra la risorsa finestra di dialogo per la pagina delle proprietà di esempio.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-113">The following illustration shows the dialog resource for the example property page.</span></span>

![finestra di dialogo della pagina delle proprietà](images/proppage.png)

<span data-ttu-id="e4ce0-115">A questo punto è possibile implementare la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="e4ce0-116">Di seguito sono descritti i metodi in **CBasePropertyPage di** cui eseguire l'override:</span><span class="sxs-lookup"><span data-stu-id="e4ce0-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="e4ce0-117">**OnConnect** viene chiamato quando il client crea la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="e4ce0-118">Imposta il **puntatore IUnknown** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="e4ce0-119">**OnActivate** viene chiamato quando viene creata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="e4ce0-120">**OnReceiveMessage viene** chiamato quando la finestra di dialogo riceve un messaggio di finestra.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="e4ce0-121">**OnApplyChanges viene** chiamato quando l'utente esegue il commit delle modifiche alle proprietà facendo clic sul **pulsante OK** **o** Applica.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="e4ce0-122">**OnDisconnect viene** chiamato quando l'utente chiude la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="e4ce0-123">La parte restante di questa esercitazione descrive ognuno di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="e4ce0-124">Successivo: [Passaggio 5. Archiviare un puntatore al filtro](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e4ce0-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ce0-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4ce0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ce0-126">Creazione di una pagina delle proprietà Filtro</span><span class="sxs-lookup"><span data-stu-id="e4ce0-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



