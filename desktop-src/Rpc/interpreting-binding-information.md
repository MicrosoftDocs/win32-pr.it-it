---
title: Interpretazione delle informazioni di binding
description: Microsoft RPC consente ai programmi client e server di accedere e interpretare le informazioni in un handle di binding.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- RPC, attività, interpretazione dell'associazione di procedura remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471734"
---
# <a name="interpreting-binding-information"></a><span data-ttu-id="15800-104">Interpretazione delle informazioni di binding</span><span class="sxs-lookup"><span data-stu-id="15800-104">Interpreting Binding Information</span></span>

<span data-ttu-id="15800-105">Microsoft RPC consente ai programmi client e server di accedere e interpretare le informazioni in un handle di binding.</span><span class="sxs-lookup"><span data-stu-id="15800-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="15800-106">Ciò non significa che è possibile o tentare di accedere direttamente al contenuto di un handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="15800-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="15800-107">Microsoft RPC fornisce funzioni che consentono di impostare e recuperare le informazioni negli handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="15800-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="15800-108">Per ottenere le informazioni in un handle di associazione, passare l'handle a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="15800-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="15800-109">Restituisce le informazioni di binding sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="15800-109">It returns the binding information as a string.</span></span> <span data-ttu-id="15800-110">Per ogni chiamata a **RpcBindingToStringBinding**, è necessario disporre di una chiamata corrispondente alla funzione [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span><span class="sxs-lookup"><span data-stu-id="15800-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="15800-111">È possibile chiamare la funzione [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) per analizzare la stringa ottenuta da [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="15800-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="15800-112">Questa funzione alloca stringhe in modo che contengano le informazioni analizzate.</span><span class="sxs-lookup"><span data-stu-id="15800-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="15800-113">Se non si desidera che analizzi un particolare elemento di informazioni di binding, passare un valore **null** come valore di tale parametro.</span><span class="sxs-lookup"><span data-stu-id="15800-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="15800-114">Assicurarsi di chiamare [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per ogni stringa allocata.</span><span class="sxs-lookup"><span data-stu-id="15800-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="15800-115">Nel frammento di codice seguente viene illustrato il modo in cui un'applicazione può chiamare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="15800-115">The following code fragment illustrates how an application might call these functions.</span></span>


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



<span data-ttu-id="15800-116">Il codice di esempio precedente chiama le funzioni [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) e [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) per ottenere e analizzare le informazioni in un handle di associazione valido.</span><span class="sxs-lookup"><span data-stu-id="15800-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="15800-117">Si noti che il valore **null** è stato passato come secondo parametro a **RpcStringBindingParse**.</span><span class="sxs-lookup"><span data-stu-id="15800-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="15800-118">In questo modo, la funzione ignorerà l'UUID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="15800-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="15800-119">Poiché non analizza l'UUID, **RpcStringBindingParse** non ne allocherà una stringa.</span><span class="sxs-lookup"><span data-stu-id="15800-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="15800-120">Questa tecnica consente all'applicazione di allocare memoria solo per le informazioni di interesse per l'analisi e l'analisi.</span><span class="sxs-lookup"><span data-stu-id="15800-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 




