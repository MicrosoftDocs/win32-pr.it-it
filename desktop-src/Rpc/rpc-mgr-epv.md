---
title: RPC_MGR_EPV (rpcdce. h)
description: Il tipo di dati RPC \_ Mgr \_ EPV definisce un vettore del punto di ingresso di gestione.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC RPC_MGR_EPV
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740215"
---
# <a name="rpc_mgr_epv"></a><span data-ttu-id="611dd-104">EPV di gestione RPC \_ \_</span><span class="sxs-lookup"><span data-stu-id="611dd-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="611dd-105">Il tipo di dati **RPC \_ Mgr \_ EPV** definisce un vettore del punto di ingresso di gestione.</span><span class="sxs-lookup"><span data-stu-id="611dd-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="611dd-106">Membri</span><span class="sxs-lookup"><span data-stu-id="611dd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="611dd-107"><span id="if-name"></span><span id="IF-NAME"></span>**If-name**</span><span class="sxs-lookup"><span data-stu-id="611dd-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-108">Specifica il nome dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="611dd-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="611dd-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**tipo restituito**</span><span class="sxs-lookup"><span data-stu-id="611dd-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-110">Specifica il tipo restituito dalla funzione **FunctionName** indicata nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="611dd-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**</span><span class="sxs-lookup"><span data-stu-id="611dd-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-112">Specifica il nome della funzione indicata nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="611dd-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span><span class="sxs-lookup"><span data-stu-id="611dd-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-114">Specifica i parametri indicati per la funzione **FunctionName** nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="611dd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="611dd-115">Remarks</span></span>

<span data-ttu-id="611dd-116">Il vettore del punto di ingresso di gestione (EPV) è una matrice di puntatori a funzione.</span><span class="sxs-lookup"><span data-stu-id="611dd-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="611dd-117">La matrice contiene i puntatori alle implementazioni delle funzioni specificate nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="611dd-118">Il numero di elementi nella matrice è impostato sul numero di funzioni specificate nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="611dd-119">Un'applicazione può avere anche più EPV, che rappresentano più implementazioni delle funzioni specificate nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="611dd-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="611dd-120">Il compilatore MIDL genera un tipo di dati **EPV** predefinito denominato \* if-name \***\_ server \_ EPV**, dove *if-name* specifica l'identificatore di interfaccia nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="611dd-121">Il compilatore MIDL Inizializza questo **EPV** predefinito in modo che contenga i puntatori a funzione per ogni routine specificata nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="611dd-122">Quando il server offre più implementazioni della stessa interfaccia, l'applicazione server deve dichiarare e inizializzare una variabile di tipo *if-name \* \* \* \_ server \_ EPV*\* per ogni implementazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="611dd-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="611dd-123">Ogni **EPV** deve contenere un punto di ingresso (puntatore a funzione) per ogni procedura definita nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="611dd-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="611dd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="611dd-124">Requirements</span></span>



| <span data-ttu-id="611dd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="611dd-125">Requirement</span></span> | <span data-ttu-id="611dd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="611dd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611dd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="611dd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="611dd-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="611dd-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="611dd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="611dd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="611dd-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="611dd-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="611dd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="611dd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="611dd-132"><dt>Rpcdce. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="611dd-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="611dd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="611dd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611dd-134">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="611dd-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="611dd-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="611dd-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="611dd-136">**RpcServerRegisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="611dd-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="611dd-137">**RpcServerUnregisterIf**</span><span class="sxs-lookup"><span data-stu-id="611dd-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="611dd-138">**RpcServerUnregisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="611dd-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





