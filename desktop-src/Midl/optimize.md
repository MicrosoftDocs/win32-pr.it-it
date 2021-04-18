---
title: Optimize (attributo)
description: L'attributo \ Optimize \ ACF viene usato per ottimizzare il livello di gradazione per i dati di marshalling.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- Optimize attribute MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299073"
---
# <a name="optimize-attribute"></a><span data-ttu-id="d5bcb-104">Optimize (attributo)</span><span class="sxs-lookup"><span data-stu-id="d5bcb-104">optimize attribute</span></span>

<span data-ttu-id="d5bcb-105">L'attributo **\[ optimize \]** ACF viene usato per ottimizzare il livello di gradazione per i dati di marshalling.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="d5bcb-106">Questa parola chiave è superceeded e non deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="d5bcb-107">Le compilazioni MIDL correnti devono invece usare [**/Oicf**](-oi.md)[**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="d5bcb-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="d5bcb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5bcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5bcb-109">*opzioni di ottimizzazione*</span><span class="sxs-lookup"><span data-stu-id="d5bcb-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="d5bcb-110">Specifica il metodo di marshalling dei dati.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="d5bcb-111">Usare "s" per il marshalling in modalità mista o "i" per il marshalling interpretato.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5bcb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5bcb-112">Remarks</span></span>

<span data-ttu-id="d5bcb-113">Questa versione di RPC fornisce due metodi per il marshalling dei dati: in modalità mista ("s") e interpretati ("i").</span><span class="sxs-lookup"><span data-stu-id="d5bcb-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="d5bcb-114">Questi metodi corrispondono alle opzioni della riga di comando [**/OS**](-os.md) e [**/OI**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="d5bcb-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="d5bcb-115">Il metodo interpretato esegue il marshalling dei dati completamente offline.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="d5bcb-116">Sebbene ciò possa ridurre notevolmente le dimensioni dello stub, le prestazioni possono essere influenzate.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="d5bcb-117">Se le prestazioni sono un problema, il metodo in modalità mista può essere l'approccio migliore.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="d5bcb-118">La modalità mista consente al compilatore MIDL di determinare tra i dati di cui verrà eseguito il marshalling inline e di cui verrà effettuato il marshalling da una chiamata a una libreria a collegamento dinamico offline.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="d5bcb-119">Se molte procedure utilizzano gli stessi tipi di dati, è possibile chiamare ripetutamente una singola procedura per effettuare il marshalling dei dati.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="d5bcb-120">In questo modo, i dati più appropriati per il marshalling inline vengono elaborati inline mentre altri dati possono essere sottoposti a marshalling in modo più efficiente offline.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="d5bcb-121">Si noti che l'attributo **\[ optimize \]** può essere utilizzato come attributo di interfaccia o come attributo Operation.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="d5bcb-122">Se viene usato come attributo di interfaccia, imposta il valore predefinito per l'intera interfaccia, eseguendo l'override delle opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="d5bcb-123">Se, tuttavia, viene utilizzato come attributo dell'operazione, influiscono solo su tale operazione, ignorando le opzioni della riga di comando e l'interfaccia predefinita.</span><span class="sxs-lookup"><span data-stu-id="d5bcb-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="d5bcb-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="d5bcb-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="d5bcb-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d5bcb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5bcb-126">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="d5bcb-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d5bcb-127">**/OI**</span><span class="sxs-lookup"><span data-stu-id="d5bcb-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="d5bcb-128">**/OS**</span><span class="sxs-lookup"><span data-stu-id="d5bcb-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="d5bcb-129">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="d5bcb-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




