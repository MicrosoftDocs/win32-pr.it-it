---
description: Trasformazione scalare utilizzata dal disegno o da InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Elemento ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316818"
---
# <a name="scalartransform-element"></a><span data-ttu-id="5d637-103">Elemento ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="5d637-103">ScalarTransform Element</span></span>

<span data-ttu-id="5d637-104">Trasformazione scalare utilizzata dal [**disegno**](drawing-element.md) o da [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="5d637-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="5d637-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="5d637-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="5d637-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5d637-106">Parent Elements</span></span>

[<span data-ttu-id="5d637-107">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="5d637-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="5d637-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="5d637-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="5d637-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5d637-109">Child Elements</span></span>

<span data-ttu-id="5d637-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="5d637-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="5d637-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="5d637-111">Attributes</span></span>



| <span data-ttu-id="5d637-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="5d637-112">Attribute</span></span> | <span data-ttu-id="5d637-113">Type</span><span class="sxs-lookup"><span data-stu-id="5d637-113">Type</span></span>           | <span data-ttu-id="5d637-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="5d637-114">Required</span></span> | <span data-ttu-id="5d637-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d637-115">Description</span></span> | <span data-ttu-id="5d637-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5d637-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="5d637-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="5d637-117">**Mat1**</span></span>  | <span data-ttu-id="5d637-118">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-118">**xs:decimal**</span></span> | <span data-ttu-id="5d637-119">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-119">Required</span></span> |             | <span data-ttu-id="5d637-120">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-120">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="5d637-121">**Mat2**</span></span>  | <span data-ttu-id="5d637-122">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-122">**xs:decimal**</span></span> | <span data-ttu-id="5d637-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-123">Required</span></span> |             | <span data-ttu-id="5d637-124">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-124">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="5d637-125">**Mat3**</span></span>  | <span data-ttu-id="5d637-126">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-126">**xs:decimal**</span></span> | <span data-ttu-id="5d637-127">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-127">Required</span></span> |             | <span data-ttu-id="5d637-128">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-128">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="5d637-129">**Mat4**</span></span>  | <span data-ttu-id="5d637-130">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-130">**xs:decimal**</span></span> | <span data-ttu-id="5d637-131">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-131">Required</span></span> |             | <span data-ttu-id="5d637-132">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-132">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="5d637-133">**Mat5**</span></span>  | <span data-ttu-id="5d637-134">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-134">**xs:decimal**</span></span> | <span data-ttu-id="5d637-135">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-135">Required</span></span> |             | <span data-ttu-id="5d637-136">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-136">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="5d637-137">**Mat6**</span></span>  | <span data-ttu-id="5d637-138">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-138">**xs:decimal**</span></span> | <span data-ttu-id="5d637-139">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-139">Required</span></span> |             | <span data-ttu-id="5d637-140">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-140">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="5d637-141">**Mat7**</span></span>  | <span data-ttu-id="5d637-142">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-142">**xs:decimal**</span></span> | <span data-ttu-id="5d637-143">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-143">Required</span></span> |             | <span data-ttu-id="5d637-144">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-144">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="5d637-145">**Mat8**</span></span>  | <span data-ttu-id="5d637-146">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-146">**xs:decimal**</span></span> | <span data-ttu-id="5d637-147">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-147">Required</span></span> |             | <span data-ttu-id="5d637-148">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-148">Any decimal number.</span></span> |
| <span data-ttu-id="5d637-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="5d637-149">**Mat9**</span></span>  | <span data-ttu-id="5d637-150">**xs: decimal**</span><span class="sxs-lookup"><span data-stu-id="5d637-150">**xs:decimal**</span></span> | <span data-ttu-id="5d637-151">Necessario</span><span class="sxs-lookup"><span data-stu-id="5d637-151">Required</span></span> |             | <span data-ttu-id="5d637-152">Qualsiasi numero decimale.</span><span class="sxs-lookup"><span data-stu-id="5d637-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="5d637-153">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5d637-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5d637-154">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5d637-154">Element type</span></span> | <span data-ttu-id="5d637-155">ComplexType [**ScalarTransformType**](scalartransformtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="5d637-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5d637-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5d637-156">Namespace</span></span>    | <span data-ttu-id="5d637-157">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="5d637-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="5d637-158">Nome schema</span><span class="sxs-lookup"><span data-stu-id="5d637-158">Schema name</span></span>  | <span data-ttu-id="5d637-159">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="5d637-159">Journal Reader</span></span>                                                              |



 

 

 



