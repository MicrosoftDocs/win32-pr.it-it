---
title: /use_epv opzione
description: L' \_ opzione/utilizza EPV indica al compilatore MIDL di generare codice stub del server che chiama la routine dell'applicazione server tramite un vettore del punto di ingresso (EPV), anziché da una chiamata statica. Non è consigliabile usare questo attributo.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv switch MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299662"
---
# <a name="use_epv-switch"></a><span data-ttu-id="4454e-105">\_opzione EPV/utilizza</span><span class="sxs-lookup"><span data-stu-id="4454e-105">/use\_epv switch</span></span>

<span data-ttu-id="4454e-106">L'opzione **/utilizza \_ EPV** indica al compilatore MIDL di generare codice stub del server che chiama la routine dell'applicazione server tramite un vettore del punto di ingresso (EPV), anziché da una chiamata statica.</span><span class="sxs-lookup"><span data-stu-id="4454e-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="4454e-107">Non è consigliabile usare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="4454e-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="4454e-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="4454e-108">Switch Options</span></span>

<span data-ttu-id="4454e-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="4454e-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4454e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4454e-110">Remarks</span></span>

<span data-ttu-id="4454e-111">In genere, le applicazioni richiedono il collegamento statico alla routine dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="4454e-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="4454e-112">Per impostazione predefinita, il compilatore MIDL genera una chiamata di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="4454e-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="4454e-113">Tuttavia, se un'applicazione richiede che lo stub del server chiami la routine dell'applicazione server usando EPV, è necessario specificare l'opzione **/utilizza \_ EPV** .</span><span class="sxs-lookup"><span data-stu-id="4454e-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="4454e-114">Quando viene specificata l'opzione **/utilizza \_ EPV** , il compilatore MIDL genera un EPV predefinito.</span><span class="sxs-lookup"><span data-stu-id="4454e-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="4454e-115">Questa EPV predefinita viene quindi utilizzata se l'applicazione non registra un altro EPV tramite la chiamata [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="4454e-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="4454e-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4454e-116">Examples</span></span>

<span data-ttu-id="4454e-117">**MIDL/utilizza \_ EPV** *nomefile \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="4454e-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="4454e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4454e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4454e-119">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="4454e-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4454e-120">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="4454e-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4454e-121">**/No \_ default \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="4454e-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="4454e-122">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="4454e-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 