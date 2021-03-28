---
title: Tipo Vector (HLSL)
description: Un vettore contiene tra uno e quattro componenti scalari; ogni componente di un vettore deve essere dello stesso tipo.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Vettore di tipo HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104995261"
---
# <a name="vector-type"></a><span data-ttu-id="620f1-104">Tipo di vettore</span><span class="sxs-lookup"><span data-stu-id="620f1-104">Vector Type</span></span>

<span data-ttu-id="620f1-105">Un vettore contiene tra uno e quattro componenti scalari; ogni componente di un vettore deve essere dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="620f1-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="620f1-106">**Nome TypeNumber**</span><span class="sxs-lookup"><span data-stu-id="620f1-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="620f1-107">Componenti</span><span class="sxs-lookup"><span data-stu-id="620f1-107">Components</span></span>



| <span data-ttu-id="620f1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="620f1-108">Item</span></span>                                                                                                                             | <span data-ttu-id="620f1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="620f1-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620f1-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="620f1-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="620f1-111">Nome singolo che contiene due parti.</span><span class="sxs-lookup"><span data-stu-id="620f1-111">A single name that contains two parts.</span></span> <span data-ttu-id="620f1-112">La prima parte è uno dei tipi [scalari](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="620f1-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="620f1-113">La seconda parte è il numero di componenti, che deve essere compreso tra 1 e 4 inclusi.</span><span class="sxs-lookup"><span data-stu-id="620f1-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="620f1-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="620f1-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="620f1-115">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="620f1-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="620f1-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="620f1-116">Examples</span></span>

<span data-ttu-id="620f1-117">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="620f1-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="620f1-118">Un vettore può essere dichiarato utilizzando anche questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="620f1-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="620f1-119">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="620f1-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="620f1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="620f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620f1-121">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="620f1-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





