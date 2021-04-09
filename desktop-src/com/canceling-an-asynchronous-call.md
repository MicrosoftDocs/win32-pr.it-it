---
title: Annullamento di una chiamata asincrona
description: Un client può annullare una chiamata asincrona in corso se l'oggetto chiamata implementa l'interfaccia ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118534"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="c7334-103">Annullamento di una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="c7334-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="c7334-104">Un client può annullare una chiamata asincrona in corso se l'oggetto chiamata implementa l'interfaccia [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="c7334-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="c7334-105">Per gli oggetti che usano il marshalling standard, **ICancelMethodCalls** è sempre disponibile per le chiamate sottoposte a marshalling.</span><span class="sxs-lookup"><span data-stu-id="c7334-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="c7334-106">Per gli oggetti che usano il marshalling personalizzato o per le chiamate a oggetti server all'interno dello stesso Apartment, questa funzionalità è disponibile solo se l'oggetto chiamata implementa **ICancelMethodCalls**.</span><span class="sxs-lookup"><span data-stu-id="c7334-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="c7334-107">Il client può annullare la chiamata in qualsiasi momento, da quando il \_ metodo Begin viene chiamato fino a quando il metodo Finish non \_ restituisce.</span><span class="sxs-lookup"><span data-stu-id="c7334-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="c7334-108">Se il client Annulla la chiamata prima di chiamare il \_ Metodo Finish, deve chiamare il metodo Finish \_ per pulire lo stato dell'oggetto call.</span><span class="sxs-lookup"><span data-stu-id="c7334-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="c7334-109">Fino a quando il client non ha eseguito questa operazione, tutte le chiamate a qualsiasi metodo Begin nell' \_ oggetto chiamata restituiranno la \_ chiamata RPC E \_ \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c7334-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="c7334-110">**Per annullare una chiamata asincrona**</span><span class="sxs-lookup"><span data-stu-id="c7334-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="c7334-111">Eseguire una query sull'oggetto chiamata per [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span><span class="sxs-lookup"><span data-stu-id="c7334-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="c7334-112">Chiamare [**ICancelMethodCalls:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), quindi chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare il puntatore ottenuto dalla chiamata [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="c7334-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="c7334-113">Se il client non ha ancora chiamato il \_ Metodo Finish, chiamarlo ora.</span><span class="sxs-lookup"><span data-stu-id="c7334-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="c7334-114">Non esiste alcuna garanzia che il server abbia interrotto effettivamente l'esecuzione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="c7334-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="c7334-115">Se l'ulteriore lavoro del client dipende da uno stato del server in cui è possibile che la chiamata non sia stata modificata, il client deve determinare tale stato prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="c7334-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7334-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7334-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7334-117">Esecuzione di una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="c7334-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 