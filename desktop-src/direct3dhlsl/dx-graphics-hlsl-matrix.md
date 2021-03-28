---
title: Tipo matrice
description: Una matrice è un tipo di dati speciale che contiene tra uno e sedici componenti. Ogni componente di una matrice deve essere dello stesso tipo.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Tipo matrice HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045524"
---
# <a name="matrix-type"></a><span data-ttu-id="b6b08-105">Tipo matrice</span><span class="sxs-lookup"><span data-stu-id="b6b08-105">Matrix Type</span></span>

<span data-ttu-id="b6b08-106">Una matrice è un tipo di dati speciale che contiene tra uno e sedici componenti.</span><span class="sxs-lookup"><span data-stu-id="b6b08-106">A matrix is a special data type that contains between one and sixteen components.</span></span> <span data-ttu-id="b6b08-107">Ogni componente di una matrice deve essere dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="b6b08-107">Every component of a matrix must be of the same type.</span></span>



|                         |
|-------------------------|
| <span data-ttu-id="b6b08-108">**Nome TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="b6b08-108">**TypeComponents Name**</span></span> |



 

## <a name="components"></a><span data-ttu-id="b6b08-109">Componenti</span><span class="sxs-lookup"><span data-stu-id="b6b08-109">Components</span></span>



| <span data-ttu-id="b6b08-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6b08-110">Item</span></span>                                                                                                                             | <span data-ttu-id="b6b08-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6b08-111">Description</span></span>                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b08-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="b6b08-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="b6b08-113">Nome singolo che contiene tre parti.</span><span class="sxs-lookup"><span data-stu-id="b6b08-113">A single name that contains three parts.</span></span> <span data-ttu-id="b6b08-114">La prima parte è uno dei tipi [scalari](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b08-114">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="b6b08-115">La seconda parte è il numero di righe.</span><span class="sxs-lookup"><span data-stu-id="b6b08-115">The second part is the number of rows.</span></span> <span data-ttu-id="b6b08-116">La terza parte è il numero di colonne.</span><span class="sxs-lookup"><span data-stu-id="b6b08-116">The third part is the number of columns.</span></span> <span data-ttu-id="b6b08-117">Il numero di righe e colonne è un numero intero positivo compreso tra 1 e 4.</span><span class="sxs-lookup"><span data-stu-id="b6b08-117">The number of rows and columns is a positive integer between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="b6b08-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="b6b08-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="b6b08-119">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="b6b08-119">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a><span data-ttu-id="b6b08-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6b08-120">Examples</span></span>

<span data-ttu-id="b6b08-121">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="b6b08-121">Here are some examples:</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="b6b08-122">Una matrice può essere dichiarata utilizzando anche questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="b6b08-122">A matrix can be declared using this syntax also:</span></span>


```
matrix <Type, Number> VariableName
```



<span data-ttu-id="b6b08-123">Il tipo di matrice utilizza le parentesi acute per specificare il tipo, il numero di righe e il numero di colonne.</span><span class="sxs-lookup"><span data-stu-id="b6b08-123">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="b6b08-124">In questo esempio viene creata una matrice a virgola mobile, con due righe e due colonne.</span><span class="sxs-lookup"><span data-stu-id="b6b08-124">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="b6b08-125">È possibile utilizzare qualsiasi tipo di dati scalari.</span><span class="sxs-lookup"><span data-stu-id="b6b08-125">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="b6b08-126">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="b6b08-126">Here is an example:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a><span data-ttu-id="b6b08-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6b08-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b08-128">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6b08-128">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





