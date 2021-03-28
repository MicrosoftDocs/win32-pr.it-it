---
title: numThreads
description: Definisce il numero di thread da eseguire in un gruppo a thread singolo quando viene inviato un compute shader (vedere sul ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399661"
---
# <a name="numthreads"></a><span data-ttu-id="06ef5-103">numThreads</span><span class="sxs-lookup"><span data-stu-id="06ef5-103">numthreads</span></span>

<span data-ttu-id="06ef5-104">Definisce il numero di thread da eseguire in un gruppo a thread singolo quando viene inviato un compute shader (vedere [**sul ID3D11DeviceContext::D la patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span><span class="sxs-lookup"><span data-stu-id="06ef5-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="06ef5-105">I valori X, Y e Z indicano le dimensioni del gruppo di thread in una direzione specifica e il totale di X \* Y \* z indica il numero di thread nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="06ef5-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="06ef5-106">La possibilità di specificare le dimensioni del gruppo di thread in tre dimensioni consente di accedere ai singoli thread in modo che le strutture di dati 2D e 3D siano logicamente.</span><span class="sxs-lookup"><span data-stu-id="06ef5-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="06ef5-107">Se, ad esempio, un compute shader sta eseguendo l'aggiunta di matrici 4x4, numThreads potrebbe essere impostato su numThreads (4, 4, 1) e l'indicizzazione nei singoli thread corrisponderà automaticamente alle voci della matrice.</span><span class="sxs-lookup"><span data-stu-id="06ef5-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="06ef5-108">Il compute shader può anche dichiarare un gruppo di thread con lo stesso numero di thread (16) utilizzando numThreads (16, 1,1), tuttavia sarà necessario calcolare la voce della matrice corrente in base al numero di thread corrente.</span><span class="sxs-lookup"><span data-stu-id="06ef5-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="06ef5-109">I valori dei parametri consentiti per **numThreads** dipendono dalla versione compute shader.</span><span class="sxs-lookup"><span data-stu-id="06ef5-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="06ef5-110">Compute Shader</span><span class="sxs-lookup"><span data-stu-id="06ef5-110">Compute Shader</span></span> | <span data-ttu-id="06ef5-111">Massimo Z</span><span class="sxs-lookup"><span data-stu-id="06ef5-111">Maximum Z</span></span> | <span data-ttu-id="06ef5-112">Numero massimo di thread (X \* Y \* Z)</span><span class="sxs-lookup"><span data-stu-id="06ef5-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="06ef5-113">cs \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="06ef5-113">cs\_4\_x</span></span>       | <span data-ttu-id="06ef5-114">1</span><span class="sxs-lookup"><span data-stu-id="06ef5-114">1</span></span>         | <span data-ttu-id="06ef5-115">768</span><span class="sxs-lookup"><span data-stu-id="06ef5-115">768</span></span>                       |
| <span data-ttu-id="06ef5-116">cs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="06ef5-116">cs\_5\_0</span></span>       | <span data-ttu-id="06ef5-117">64</span><span class="sxs-lookup"><span data-stu-id="06ef5-117">64</span></span>        | <span data-ttu-id="06ef5-118">1024</span><span class="sxs-lookup"><span data-stu-id="06ef5-118">1024</span></span>                      |



 

<span data-ttu-id="06ef5-119">Nella figura seguente viene illustrata la relazione tra i parametri passati a [**sul ID3D11DeviceContext::D di patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo numThreads, numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="06ef5-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

<span data-ttu-id="06ef5-121">Questo attributo è supportato nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="06ef5-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="06ef5-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="06ef5-122">Vertex</span></span> | <span data-ttu-id="06ef5-123">Hull</span><span class="sxs-lookup"><span data-stu-id="06ef5-123">Hull</span></span> | <span data-ttu-id="06ef5-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="06ef5-124">Domain</span></span> | <span data-ttu-id="06ef5-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="06ef5-125">Geometry</span></span> | <span data-ttu-id="06ef5-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="06ef5-126">Pixel</span></span> | <span data-ttu-id="06ef5-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="06ef5-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="06ef5-128">x</span><span class="sxs-lookup"><span data-stu-id="06ef5-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="06ef5-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06ef5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06ef5-130">Attributi del modello di shader 5</span><span class="sxs-lookup"><span data-stu-id="06ef5-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="06ef5-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="06ef5-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 