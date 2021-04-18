---
description: In questo argomento viene descritto come implementare un componente come libreria di collegamento dinamico (DLL) in Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funzioni DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303747"
---
# <a name="dll-functions"></a><span data-ttu-id="980f0-103">Funzioni DLL</span><span class="sxs-lookup"><span data-stu-id="980f0-103">DLL Functions</span></span>

<span data-ttu-id="980f0-104">In questo argomento viene descritto come implementare un componente come libreria di collegamento dinamico (DLL) in Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="980f0-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="980f0-105">Una DLL deve implementare le funzioni seguenti in modo che sia possibile registrarla, annullarne la registrazione e caricarla in memoria.</span><span class="sxs-lookup"><span data-stu-id="980f0-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="980f0-106">[*DllMain*](/windows/desktop/Dlls/dllmain): il punto di ingresso della dll.</span><span class="sxs-lookup"><span data-stu-id="980f0-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="980f0-107">Il nome *DllMain* è un segnaposto per il nome della funzione definita dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="980f0-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="980f0-108">L'implementazione di DirectShow usa il nome **DllEntryPoint**.</span><span class="sxs-lookup"><span data-stu-id="980f0-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="980f0-109">Per ulteriori informazioni, vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="980f0-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="980f0-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): crea un'istanza di class factory.</span><span class="sxs-lookup"><span data-stu-id="980f0-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="980f0-111">Descritto nelle sezioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="980f0-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="980f0-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): esegue una query per determinare se la dll può essere scaricata in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="980f0-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="980f0-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crea le voci del registro di sistema per la dll.</span><span class="sxs-lookup"><span data-stu-id="980f0-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="980f0-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): rimuove le voci del registro di sistema per la dll.</span><span class="sxs-lookup"><span data-stu-id="980f0-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="980f0-115">Di queste, le prime tre sono implementate da DirectShow.</span><span class="sxs-lookup"><span data-stu-id="980f0-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="980f0-116">Se il modello Factory fornisce una funzione di inizializzazione nella variabile membro [**\_ lpfnInit m**](cfactorytemplate-m-lpfninit.md) , tale funzione viene chiamata dall'interno della funzione del punto di ingresso della dll.</span><span class="sxs-lookup"><span data-stu-id="980f0-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="980f0-117">Per ulteriori informazioni su quando il sistema chiama la funzione del punto di ingresso della DLL, vedere [*DllMain*](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="980f0-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="980f0-118">È necessario implementare [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), ma DirectShow fornisce una funzione denominata [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) che esegue le operazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="980f0-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="980f0-119">Il componente può semplicemente eseguire il wrapping di questa funzione, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="980f0-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="980f0-120">Tuttavia, all'interno di [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) è possibile personalizzare il processo di registrazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="980f0-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="980f0-121">Se la DLL contiene un filtro, potrebbe essere necessario eseguire alcune operazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="980f0-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="980f0-122">Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="980f0-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="980f0-123">Nel file di definizione del modulo (con estensione def) esportare tutte le funzioni DLL eccetto la funzione del punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="980f0-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="980f0-124">Di seguito è riportato un esempio di file con estensione def:</span><span class="sxs-lookup"><span data-stu-id="980f0-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="980f0-125">È possibile registrare la DLL utilizzando l'utilità Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="980f0-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="980f0-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="980f0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="980f0-127">Come creare una DLL di filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="980f0-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
