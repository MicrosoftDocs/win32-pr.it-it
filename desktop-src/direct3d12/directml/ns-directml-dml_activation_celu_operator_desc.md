---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Esegue la funzione di attivazione di unità lineare esponenziale (CELU) continuamente differenziabile su ogni elemento in *InputTensor*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: d474bd44c8a830117bb62927f4bda954a753b612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320280"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="47cfd-103">Struttura DML_ACTIVATION_CELU_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="47cfd-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="47cfd-104">Esegue la funzione di attivazione di unità lineare esponenziale (CELU) continuamente differenziabile su ogni elemento in *InputTensor*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="47cfd-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="47cfd-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="47cfd-105">Where:</span></span>
* <span data-ttu-id="47cfd-106">Exp (x) è la funzione di elevamento a potenza naturale</span><span class="sxs-lookup"><span data-stu-id="47cfd-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="47cfd-107">Max (a, b) restituisce il maggiore tra i due valori a, b</span><span class="sxs-lookup"><span data-stu-id="47cfd-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="47cfd-108">min (a, b) restituisce il minore dei due valori a, b</span><span class="sxs-lookup"><span data-stu-id="47cfd-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="47cfd-109">Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output è autorizzato ad alias *InputTensor* durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="47cfd-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47cfd-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="47cfd-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="47cfd-111">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="47cfd-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="47cfd-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47cfd-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="47cfd-113">Members</span><span class="sxs-lookup"><span data-stu-id="47cfd-113">Members</span></span>

`InputTensor`

<span data-ttu-id="47cfd-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="47cfd-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="47cfd-115">Tensore di input da cui eseguire la lettura.</span><span class="sxs-lookup"><span data-stu-id="47cfd-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="47cfd-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="47cfd-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="47cfd-117">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="47cfd-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="47cfd-118">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="47cfd-118">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="47cfd-119">Coefficiente alfa.</span><span class="sxs-lookup"><span data-stu-id="47cfd-119">The alpha coefficient.</span></span> <span data-ttu-id="47cfd-120">Un valore predefinito tipico per questo valore è 1,0.</span><span class="sxs-lookup"><span data-stu-id="47cfd-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="47cfd-121">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="47cfd-121">Availability</span></span>
<span data-ttu-id="47cfd-122">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="47cfd-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="47cfd-123">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="47cfd-123">Tensor constraints</span></span>
<span data-ttu-id="47cfd-124">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="47cfd-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="47cfd-125">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="47cfd-125">Tensor support</span></span>
| <span data-ttu-id="47cfd-126">Tensore</span><span class="sxs-lookup"><span data-stu-id="47cfd-126">Tensor</span></span> | <span data-ttu-id="47cfd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="47cfd-127">Kind</span></span> | <span data-ttu-id="47cfd-128">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="47cfd-128">Supported Dimension Counts</span></span> | <span data-ttu-id="47cfd-129">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="47cfd-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="47cfd-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="47cfd-130">InputTensor</span></span> | <span data-ttu-id="47cfd-131">Input</span><span class="sxs-lookup"><span data-stu-id="47cfd-131">Input</span></span> | <span data-ttu-id="47cfd-132">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="47cfd-132">1 to 8</span></span> | <span data-ttu-id="47cfd-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="47cfd-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="47cfd-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="47cfd-134">OutputTensor</span></span> | <span data-ttu-id="47cfd-135">Output</span><span class="sxs-lookup"><span data-stu-id="47cfd-135">Output</span></span> | <span data-ttu-id="47cfd-136">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="47cfd-136">1 to 8</span></span> | <span data-ttu-id="47cfd-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="47cfd-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="47cfd-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47cfd-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="47cfd-139">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="47cfd-139">**Header**</span></span> | <span data-ttu-id="47cfd-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="47cfd-140">directml.h</span></span> |