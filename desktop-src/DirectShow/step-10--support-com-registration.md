---
description: Passaggio 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Passaggio 10. Supporto della registrazione COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314406"
---
# <a name="step-10-support-com-registration"></a><span data-ttu-id="7fd4c-104">Passaggio 10.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-104">Step 10.</span></span> <span data-ttu-id="7fd4c-105">Supporto della registrazione COM</span><span class="sxs-lookup"><span data-stu-id="7fd4c-105">Support COM Registration</span></span>

<span data-ttu-id="7fd4c-106">L'ultima attività rimanente è supportare la registrazione COM, in modo che il frame della proprietà possa creare nuove istanze della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-106">The last remaining task is to support COM registration, so that the property frame can create new instances of your property page.</span></span> <span data-ttu-id="7fd4c-107">Aggiungere un'altra voce [**CFactoryTemplate**](cfactorytemplate.md) alla matrice *di \_ modelli g* globale, che viene usata per registrare tutti gli oggetti com nella dll.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-107">Add another [**CFactoryTemplate**](cfactorytemplate.md) entry to the global *g\_Templates* array, which is used to register all of the COM objects in your DLL.</span></span> <span data-ttu-id="7fd4c-108">Non includere le informazioni di configurazione del filtro per la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-108">Do not include any filter set-up information for the property page.</span></span>


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



<span data-ttu-id="7fd4c-109">Se si dichiara *g \_ cTemplates* come illustrato nel codice seguente, il valore corretto verrà automaticamente in base alle dimensioni della matrice:</span><span class="sxs-lookup"><span data-stu-id="7fd4c-109">If you declare *g\_cTemplates* as shown in the following code, then it automatically has the correct value based on the array size:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



<span data-ttu-id="7fd4c-110">Aggiungere inoltre un metodo statico `CreateInstance` alla classe della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-110">Also, add a static `CreateInstance` method to the property page class.</span></span> <span data-ttu-id="7fd4c-111">È possibile denominare il metodo in qualsiasi modo desiderato, ma la firma deve corrispondere a quella illustrata nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="7fd4c-111">You can name the method anything that you prefer, but the signature must match the one shown the following example:</span></span>


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



<span data-ttu-id="7fd4c-112">Per eseguire il test della pagina delle proprietà, registrare la DLL e quindi caricare il filtro in GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-112">To test the property page, register the DLL and then load the filter in GraphEdit.</span></span> <span data-ttu-id="7fd4c-113">Fare clic con il pulsante destro del mouse sul filtro e selezionare **Proprietà filtro**.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-113">Right-click the filter and select **Filter Properties**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fd4c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fd4c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fd4c-115">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="7fd4c-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="7fd4c-116">Come creare una DLL di filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="7fd4c-116">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 



