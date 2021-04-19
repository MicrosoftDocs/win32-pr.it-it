---
description: Passaggio 3.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Passaggio 3. Supporta QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317223"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="f64a1-104">Passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="f64a1-104">Step 3.</span></span> <span data-ttu-id="f64a1-105">Supporta QueryInterface</span><span class="sxs-lookup"><span data-stu-id="f64a1-105">Support QueryInterface</span></span>

<span data-ttu-id="f64a1-106">Per esporre le nuove interfacce del filtro ai client, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f64a1-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="f64a1-107">Includere la macro [**Declare \_ IUnknown**](declare-iunknown.md) nella sezione public Declaration del filtro:</span><span class="sxs-lookup"><span data-stu-id="f64a1-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="f64a1-108">Eseguire l'override di [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per verificare la IID delle due interfacce:</span><span class="sxs-lookup"><span data-stu-id="f64a1-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
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

    

<span data-ttu-id="f64a1-109">Successivo: [passaggio 4. Creare la pagina delle proprietà](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="f64a1-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f64a1-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f64a1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f64a1-111">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="f64a1-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="f64a1-112">Come implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="f64a1-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



