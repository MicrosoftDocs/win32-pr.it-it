---
description: Esporre le nuove interfacce di un filtro ai client come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Passaggio 3. Supporto di QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410024"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="c46d3-104">Passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="c46d3-104">Step 3.</span></span> <span data-ttu-id="c46d3-105">Supporto di QueryInterface</span><span class="sxs-lookup"><span data-stu-id="c46d3-105">Support QueryInterface</span></span>

<span data-ttu-id="c46d3-106">Per esporre le nuove interfacce del filtro ai client, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c46d3-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="c46d3-107">Includere la macro [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) nella sezione della dichiarazione pubblica del filtro:</span><span class="sxs-lookup"><span data-stu-id="c46d3-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="c46d3-108">Eseguire [**l'override di CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per verificare la presenza degli ID delle due interfacce:</span><span class="sxs-lookup"><span data-stu-id="c46d3-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

<span data-ttu-id="c46d3-109">Passaggio [4. Creare la pagina delle proprietà](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="c46d3-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c46d3-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c46d3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c46d3-111">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="c46d3-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="c46d3-112">Come implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="c46d3-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



