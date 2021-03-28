---
title: trasposizione
description: Traspone la matrice di input specificata.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- Trasponi HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399135"
---
# <a name="transpose"></a><span data-ttu-id="6adba-104">trasposizione</span><span class="sxs-lookup"><span data-stu-id="6adba-104">transpose</span></span>

<span data-ttu-id="6adba-105">Traspone la matrice di input specificata.</span><span class="sxs-lookup"><span data-stu-id="6adba-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="6adba-106">RET Transpose (*x*)</span><span class="sxs-lookup"><span data-stu-id="6adba-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="6adba-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6adba-107">Parameters</span></span>



| <span data-ttu-id="6adba-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6adba-108">Item</span></span>                                                   | <span data-ttu-id="6adba-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6adba-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="6adba-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="6adba-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6adba-111">\[nella \] matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="6adba-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6adba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6adba-112">Return Value</span></span>

<span data-ttu-id="6adba-113">Valore trasposto dal parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="6adba-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="6adba-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6adba-114">Remarks</span></span>

<span data-ttu-id="6adba-115">Se le dimensioni della matrice di origine sono  *colonne* di righe, la matrice risultante è costituita da *righe* di *colonne* .</span><span class="sxs-lookup"><span data-stu-id="6adba-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="6adba-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="6adba-116">Type Description</span></span>



| <span data-ttu-id="6adba-117">Nome</span><span class="sxs-lookup"><span data-stu-id="6adba-117">Name</span></span> | [<span data-ttu-id="6adba-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="6adba-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6adba-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="6adba-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="6adba-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6adba-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6adba-121">*x*</span><span class="sxs-lookup"><span data-stu-id="6adba-121">*x*</span></span>  | [<span data-ttu-id="6adba-122">**matrice**</span><span class="sxs-lookup"><span data-stu-id="6adba-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6adba-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="6adba-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="6adba-124">any</span><span class="sxs-lookup"><span data-stu-id="6adba-124">any</span></span>                                                                                    |
| <span data-ttu-id="6adba-125">RET</span><span class="sxs-lookup"><span data-stu-id="6adba-125">ret</span></span>  | [<span data-ttu-id="6adba-126">**matrice**</span><span class="sxs-lookup"><span data-stu-id="6adba-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6adba-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="6adba-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="6adba-128">righe = lo stesso numero di colonne dell'input *x*, colonne = lo stesso numero di righe dell'input *x*</span><span class="sxs-lookup"><span data-stu-id="6adba-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6adba-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="6adba-129">Minimum Shader Model</span></span>

<span data-ttu-id="6adba-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="6adba-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6adba-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6adba-131">Shader Model</span></span>                                                                       | <span data-ttu-id="6adba-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="6adba-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6adba-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="6adba-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="6adba-134">sì</span><span class="sxs-lookup"><span data-stu-id="6adba-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6adba-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6adba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6adba-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6adba-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

