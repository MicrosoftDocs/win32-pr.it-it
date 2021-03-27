---
title: Tipo di buffer
description: Utilizzare la sintassi seguente per dichiarare una variabile del buffer.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Tipo di buffer HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046944"
---
# <a name="buffer-type"></a><span data-ttu-id="5a9f4-104">Tipo di buffer</span><span class="sxs-lookup"><span data-stu-id="5a9f4-104">Buffer Type</span></span>

<span data-ttu-id="5a9f4-105">Utilizzare la sintassi seguente per dichiarare una variabile del buffer.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="5a9f4-106">Nome del *tipo* di<del buffer >  ;</span><span class="sxs-lookup"><span data-stu-id="5a9f4-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5a9f4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a9f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9f4-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span><span class="sxs-lookup"><span data-stu-id="5a9f4-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="5a9f4-109">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="5a9f4-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="5a9f4-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="5a9f4-111">Uno dei tipi [Scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md)e some [Matrix](dx-graphics-hlsl-matrix.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="5a9f4-112">È possibile dichiarare una variabile di buffer con una matrice purché si trovino in quantità a 4 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="5a9f4-113">Quindi, è possibile scrivere `Buffer<float2x2>` .</span><span class="sxs-lookup"><span data-stu-id="5a9f4-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="5a9f4-114">Ma `Buffer<float4x4>` è troppo grande e il compilatore genererà un errore.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="5a9f4-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="5a9f4-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="5a9f4-116">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="5a9f4-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="5a9f4-117">Example</span></span>

<span data-ttu-id="5a9f4-118">Di seguito è riportato un esempio di una dichiarazione di buffer dal file PipesGS. FX nell' [esempio PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="5a9f4-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="5a9f4-119">I dati vengono letti da un buffer usando una versione di overload della funzione intrinseca [**Load**](dx-graphics-hlsl-to-load.md) HLSL che accetta un parametro di input (un indice Integer).</span><span class="sxs-lookup"><span data-stu-id="5a9f4-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="5a9f4-120">È possibile accedere a un buffer come una matrice di elementi; Pertanto, in questo esempio viene letto il secondo elemento.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="5a9f4-121">Usare la [fase Stream-output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) per restituire i dati in un buffer.</span><span class="sxs-lookup"><span data-stu-id="5a9f4-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a9f4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a9f4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9f4-123">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a9f4-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 