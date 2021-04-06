---
title: parametro/Server
description: Il parametro/Server indica al compilatore MIDL di generare file di origine C sul lato server per un'interfaccia RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server-switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045758"
---
# <a name="server-switch"></a><span data-ttu-id="b3a0b-104">parametro/Server</span><span class="sxs-lookup"><span data-stu-id="b3a0b-104">/server switch</span></span>

<span data-ttu-id="b3a0b-105">Il parametro **/Server** indica al compilatore MIDL di generare file di origine C sul lato server per un'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="b3a0b-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="b3a0b-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="b3a0b-107"><span id="stub"></span><span id="STUB"></span>Stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b3a0b-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b3a0b-108">Genera i file sul lato server.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b3a0b-109"><span id="none"></span><span id="NONE"></span>nessuno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b3a0b-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="b3a0b-110">Non genera file sul lato server.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3a0b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3a0b-111">Remarks</span></span>

<span data-ttu-id="b3a0b-112">Se non si specifica l'opzione **/Server** , il compilatore MIDL genera il file stub del server.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="b3a0b-113">Questa opzione non influisce sulle interfacce OLE.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="b3a0b-114">L'opzione **None** non comporta la generazione di file.</span><span class="sxs-lookup"><span data-stu-id="b3a0b-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="b3a0b-115">L'opzione **/Server** ha la precedenza sull'opzione **/sstub**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="b3a0b-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3a0b-116">Examples</span></span>

<span data-ttu-id="b3a0b-117">**non MIDL, nessuno**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-117">**midl /server none**</span></span>

<span data-ttu-id="b3a0b-118">**Stub di MIDL/server**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="b3a0b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3a0b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a0b-120">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="b3a0b-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b3a0b-121">**/client**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="b3a0b-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="b3a0b-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




