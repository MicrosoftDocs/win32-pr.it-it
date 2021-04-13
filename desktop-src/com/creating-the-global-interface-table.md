---
title: Creazione della tabella dell'interfaccia globale
description: Creazione della tabella dell'interfaccia globale
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399796"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="ddcd8-103">Creazione della tabella dell'interfaccia globale</span><span class="sxs-lookup"><span data-stu-id="ddcd8-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="ddcd8-104">Utilizzare la chiamata seguente per creare l'oggetto tabella dell'interfaccia globale e ottenere un puntatore a [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span><span class="sxs-lookup"><span data-stu-id="ddcd8-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="ddcd8-105">Quando si crea l'oggetto tabella dell'interfaccia globale usando la chiamata precedente, è necessario collegarsi alla libreria uuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="ddcd8-106">Questa operazione risolverà i simboli esterni CLSID \_ StdGlobalInterfaceTable e IID \_ IGlobalInterfaceTable.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="ddcd8-107">Esiste una singola istanza della tabella dell'interfaccia globale per ogni processo, quindi tutte le chiamate a questa funzione in un processo restituiscono la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="ddcd8-108">Dopo la chiamata alla funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , registrare l'interfaccia dall'Apartment in cui risiede con una chiamata al metodo [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) .</span><span class="sxs-lookup"><span data-stu-id="ddcd8-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="ddcd8-109">Questo metodo fornisce un cookie che identifica l'interfaccia e la relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="ddcd8-110">Un Apartment che cerca un puntatore a questa interfaccia chiama il metodo [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) con questo cookie e l'implementazione fornisce quindi un puntatore di interfaccia all'Apartment chiamante.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="ddcd8-111">Per revocare la registrazione globale dell'interfaccia, qualsiasi Apartment può chiamare il metodo [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .</span><span class="sxs-lookup"><span data-stu-id="ddcd8-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="ddcd8-112">Un semplice esempio di utilizzo di [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) è quando si desidera passare un puntatore a un'interfaccia su un oggetto in un Apartment a thread singolo (sta) a un thread di lavoro in un altro Apartment.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="ddcd8-113">Anziché dover effettuare il marshalling in un flusso e passare il flusso al thread di lavoro come parametro di thread, **IGlobalInterfaceTable** consente di passare semplicemente un cookie.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="ddcd8-114">Quando si registra l'interfaccia nella tabella dell'interfaccia globale, si ottiene un cookie che è possibile usare anziché passare il puntatore effettivo (ogni volta che è necessario passare il puntatore), a un parametro non di metodo che passa a un altro Apartment (come parametro a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) tramite [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) o alla memoria in-process accessibile all'esterno dell'Apartment.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="ddcd8-115">È necessario prestare attenzione perché l'uso delle interfacce globali impone un carico aggiuntivo al programmatore di gestire i problemi, ad esempio race condition ed esclusioni reciproche, associati all'accesso allo stato globale da più thread contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="ddcd8-116">COM fornisce un'implementazione standard dell'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="ddcd8-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="ddcd8-117">Si consiglia vivamente di utilizzare questa implementazione standard perché fornisce funzionalità thread-safe complete.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddcd8-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddcd8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddcd8-119">Quando usare la tabella dell'interfaccia globale</span><span class="sxs-lookup"><span data-stu-id="ddcd8-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 