---
description: Trasformazione scalare usata da Drawing o InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Elemento ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432433"
---
# <a name="scalartransform-element"></a><span data-ttu-id="e8a25-103">Elemento ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="e8a25-103">ScalarTransform Element</span></span>

<span data-ttu-id="e8a25-104">Trasformazione scalare usata da [**Drawing o**](drawing-element.md) [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="e8a25-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="e8a25-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="e8a25-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="e8a25-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e8a25-106">Parent Elements</span></span>

[<span data-ttu-id="e8a25-107">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="e8a25-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="e8a25-108">**Inkword**</span><span class="sxs-lookup"><span data-stu-id="e8a25-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="e8a25-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e8a25-109">Child Elements</span></span>

<span data-ttu-id="e8a25-110">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="e8a25-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="e8a25-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="e8a25-111">Attributes</span></span>



| <span data-ttu-id="e8a25-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="e8a25-112">Attribute</span></span> | <span data-ttu-id="e8a25-113">Type</span><span class="sxs-lookup"><span data-stu-id="e8a25-113">Type</span></span>           | <span data-ttu-id="e8a25-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-114">Required</span></span> | <span data-ttu-id="e8a25-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8a25-115">Description</span></span> | <span data-ttu-id="e8a25-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e8a25-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="e8a25-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="e8a25-117">**Mat1**</span></span>  | <span data-ttu-id="e8a25-118">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-118">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-119">Required</span></span> |             | <span data-ttu-id="e8a25-120">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-120">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="e8a25-121">**Mat2**</span></span>  | <span data-ttu-id="e8a25-122">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-122">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-123">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-123">Required</span></span> |             | <span data-ttu-id="e8a25-124">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-124">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="e8a25-125">**Mat3**</span></span>  | <span data-ttu-id="e8a25-126">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-126">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-127">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-127">Required</span></span> |             | <span data-ttu-id="e8a25-128">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-128">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="e8a25-129">**Mat4**</span></span>  | <span data-ttu-id="e8a25-130">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-130">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-131">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-131">Required</span></span> |             | <span data-ttu-id="e8a25-132">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-132">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="e8a25-133">**Mat5**</span></span>  | <span data-ttu-id="e8a25-134">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-134">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-135">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-135">Required</span></span> |             | <span data-ttu-id="e8a25-136">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-136">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="e8a25-137">**Mat6**</span></span>  | <span data-ttu-id="e8a25-138">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-138">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-139">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-139">Required</span></span> |             | <span data-ttu-id="e8a25-140">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-140">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="e8a25-141">**Mat7**</span></span>  | <span data-ttu-id="e8a25-142">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-142">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-143">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-143">Required</span></span> |             | <span data-ttu-id="e8a25-144">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-144">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="e8a25-145">**Mat8**</span></span>  | <span data-ttu-id="e8a25-146">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-146">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-147">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-147">Required</span></span> |             | <span data-ttu-id="e8a25-148">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-148">Any decimal number.</span></span> |
| <span data-ttu-id="e8a25-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="e8a25-149">**Mat9**</span></span>  | <span data-ttu-id="e8a25-150">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="e8a25-150">**xs:decimal**</span></span> | <span data-ttu-id="e8a25-151">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e8a25-151">Required</span></span> |             | <span data-ttu-id="e8a25-152">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="e8a25-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="e8a25-153">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e8a25-153">Element Information</span></span>



| <span data-ttu-id="e8a25-154">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8a25-154">Element</span></span>      | <span data-ttu-id="e8a25-155">valore</span><span class="sxs-lookup"><span data-stu-id="e8a25-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="e8a25-156">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e8a25-156">Element type</span></span> | <span data-ttu-id="e8a25-157">[**ComplexType ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="e8a25-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e8a25-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8a25-158">Namespace</span></span>    | <span data-ttu-id="e8a25-159">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="e8a25-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="e8a25-160">Nome schema</span><span class="sxs-lookup"><span data-stu-id="e8a25-160">Schema name</span></span>  | <span data-ttu-id="e8a25-161">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="e8a25-161">Journal Reader</span></span>                                                              |



 

 

 



