---
title: /no_default_epv opzione
description: L' \_ \_ opzione EPV predefinita/No indica al compilatore MIDL di non generare un vettore del punto di ingresso predefinito (EPV). Non è consigliabile usare questo attributo.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv switch MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956385"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="0f84c-105">\_ \_ opzione EPV predefinita/No</span><span class="sxs-lookup"><span data-stu-id="0f84c-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="0f84c-106">L' **opzione \_ \_ EPV predefinita/No** indica al compilatore MIDL di non generare un vettore del punto di ingresso predefinito (EPV).</span><span class="sxs-lookup"><span data-stu-id="0f84c-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="0f84c-107">Non è consigliabile usare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="0f84c-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="0f84c-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="0f84c-108">Switch Options</span></span>

<span data-ttu-id="0f84c-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="0f84c-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f84c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f84c-110">Remarks</span></span>

<span data-ttu-id="0f84c-111">In questo caso, l'applicazione deve registrare un EPV con la chiamata [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="0f84c-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="0f84c-112">Confrontare questa opzione con l'opzione [**/utilizza \_ EPV**](-use-epv.md)</span><span class="sxs-lookup"><span data-stu-id="0f84c-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="0f84c-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f84c-113">Examples</span></span>

<span data-ttu-id="0f84c-114">**MIDL/No \_ default \_ EPV filename. idl**</span><span class="sxs-lookup"><span data-stu-id="0f84c-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0f84c-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f84c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f84c-116">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="0f84c-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0f84c-117">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="0f84c-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0f84c-118">**\_EPV/utilizza**</span><span class="sxs-lookup"><span data-stu-id="0f84c-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="0f84c-119">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="0f84c-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 