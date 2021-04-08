---
description: I provider possono chiamare i metodi implementati da WMI all'interno delle implementazioni del metodo.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Esecuzione di chiamate a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050061"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="5d118-103">Esecuzione di chiamate a WMI</span><span class="sxs-lookup"><span data-stu-id="5d118-103">Making Calls to WMI</span></span>

<span data-ttu-id="5d118-104">I provider possono chiamare i metodi implementati da WMI all'interno delle implementazioni del metodo.</span><span class="sxs-lookup"><span data-stu-id="5d118-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="5d118-105">Tuttavia, esistono considerazioni speciali quando un provider chiama l'implementazione WMI di un metodo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) dall'interno della propria implementazione dello stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="5d118-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="5d118-106">Queste considerazioni sono importanti a prescindere dal fatto che il provider chiami la versione sincrona o asincrona del metodo.</span><span class="sxs-lookup"><span data-stu-id="5d118-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="5d118-107">Ogni metodo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che un provider può implementare ha un parametro *pctX* , un puntatore a un'implementazione dell'interfaccia [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="5d118-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="5d118-108">Quando WMI chiama il provider, WMI passa un puntatore valido in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5d118-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="5d118-109">Un provider deve sempre passare questo stesso puntatore in tutte le chiamate a WMI effettuate durante la manutenzione delle richieste.</span><span class="sxs-lookup"><span data-stu-id="5d118-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="5d118-110">Se si trascura di impostare *pctX* in modo appropriato, WMI può avviare un ciclo infinito.</span><span class="sxs-lookup"><span data-stu-id="5d118-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="5d118-111">Nell'esempio di codice seguente viene illustrato il modo corretto per chiamare l'implementazione WMI di [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) dall'interno di un'implementazione di [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="5d118-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="5d118-112">Nell'esempio di codice C++ in questo argomento sono necessari i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="5d118-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="5d118-113">I provider di istanze, classi e proprietà non devono eseguire alcuna chiamata a WMI che richiede la modifica dei dati durante la manutenzione di una richiesta di lettura.</span><span class="sxs-lookup"><span data-stu-id="5d118-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="5d118-114">Gli unici provider che sono eccezioni a questa regola sono i provider di push.</span><span class="sxs-lookup"><span data-stu-id="5d118-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="5d118-115">Un provider di push è un provider di classi che archivia i dati nel repository WMI e si basa su WMI per gestire le richieste provenienti dai client.</span><span class="sxs-lookup"><span data-stu-id="5d118-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="5d118-116">Durante la manutenzione di una richiesta di lettura, un provider di push può aggiornare il repository WMI, ma è necessario impostare il parametro *è* sull' **aggiornamento del \_ proprietario del flag \_ \_ WBEM** nella chiamata [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) appropriata.</span><span class="sxs-lookup"><span data-stu-id="5d118-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="5d118-117">I provider di eventi non devono apportare modifiche alle classi durante la manutenzione di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d118-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="5d118-118">Non possono anche emettere chiamate relative agli eventi, ad esempio la modifica di un filtro eventi.</span><span class="sxs-lookup"><span data-stu-id="5d118-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d118-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d118-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d118-120">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="5d118-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="5d118-121">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5d118-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="5d118-122">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="5d118-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



