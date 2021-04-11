---
title: opzione/client
description: L'opzione/client indica al compilatore MIDL di generare file di origine C sul lato client per un'interfaccia RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client switch MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334575"
---
# <a name="client-switch"></a><span data-ttu-id="b7b53-104">opzione/client</span><span class="sxs-lookup"><span data-stu-id="b7b53-104">/client switch</span></span>

<span data-ttu-id="b7b53-105">L'opzione **/client** indica al compilatore MIDL di generare file di origine C sul lato client per un'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="b7b53-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="b7b53-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="b7b53-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="b7b53-107"><span id="stub"></span><span id="STUB"></span>Stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b7b53-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b7b53-108">Genera i file sul lato client.</span><span class="sxs-lookup"><span data-stu-id="b7b53-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b7b53-109"><span id="none"></span><span id="NONE"></span>nessuno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b7b53-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b7b53-110">Non genera alcun file lato client.</span><span class="sxs-lookup"><span data-stu-id="b7b53-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7b53-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7b53-111">Remarks</span></span>

<span data-ttu-id="b7b53-112">Quando l'opzione **/client** non è specificata, il compilatore MIDL genera il file stub del client.</span><span class="sxs-lookup"><span data-stu-id="b7b53-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="b7b53-113">Questa opzione non influisce sulle interfacce OLE.</span><span class="sxs-lookup"><span data-stu-id="b7b53-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="b7b53-114">L'opzione **/client** ha la precedenza sull'opzione [**/cstub**](-cstub.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b53-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="b7b53-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="b7b53-115">Examples</span></span>

<span data-ttu-id="b7b53-116">**MIDL/client None nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="b7b53-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="b7b53-117">**nome file stub MIDL/client. idl**</span><span class="sxs-lookup"><span data-stu-id="b7b53-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b7b53-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7b53-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b53-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="b7b53-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="b7b53-120">**/Server**</span><span class="sxs-lookup"><span data-stu-id="b7b53-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="b7b53-121">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="b7b53-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




