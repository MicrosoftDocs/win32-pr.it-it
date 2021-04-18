---
description: Rappresenta una matrice 3x3 che, a sua volta, rappresenta una trasformazione affine.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Classe InkTransform (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319168"
---
# <a name="inktransform-class"></a><span data-ttu-id="1ede2-103">Classe InkTransform</span><span class="sxs-lookup"><span data-stu-id="1ede2-103">InkTransform class</span></span>

<span data-ttu-id="1ede2-104">Rappresenta una matrice 3x3 che, a sua volta, rappresenta una trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="1ede2-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="1ede2-105">**InkTransform** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1ede2-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="1ede2-106">Metodi</span><span class="sxs-lookup"><span data-stu-id="1ede2-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ede2-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ede2-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ede2-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1ede2-108">Methods</span></span>

<span data-ttu-id="1ede2-109">La classe **InkTransform** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1ede2-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="1ede2-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="1ede2-110">Method</span></span>                                                  | <span data-ttu-id="1ede2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ede2-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ede2-112">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="1ede2-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="1ede2-113">Recupera **InkTransform** come 6 float.</span><span class="sxs-lookup"><span data-stu-id="1ede2-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="1ede2-114">**Riflettere**</span><span class="sxs-lookup"><span data-stu-id="1ede2-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="1ede2-115">Riflette la trasformazione in direzioni orizzontali o verticali.</span><span class="sxs-lookup"><span data-stu-id="1ede2-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="1ede2-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="1ede2-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="1ede2-117">Reimposta lo stato originale della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="1ede2-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="1ede2-118">**Ruota**</span><span class="sxs-lookup"><span data-stu-id="1ede2-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="1ede2-119">Ruota la trasformazione in base a un angolo misurato in gradi e, facoltativamente, specifica un punto centrale per la rotazione.</span><span class="sxs-lookup"><span data-stu-id="1ede2-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="1ede2-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="1ede2-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="1ede2-121">Ridimensiona la trasformazione in base ai fattori X e Y.</span><span class="sxs-lookup"><span data-stu-id="1ede2-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="1ede2-122">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="1ede2-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="1ede2-123">Modifica **InkTransform** utilizzando 6 float.</span><span class="sxs-lookup"><span data-stu-id="1ede2-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="1ede2-124">**Taglio**</span><span class="sxs-lookup"><span data-stu-id="1ede2-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="1ede2-125">Applica una cesoia con i fattori orizzontali e verticali specificati.</span><span class="sxs-lookup"><span data-stu-id="1ede2-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="1ede2-126">**Traduci**</span><span class="sxs-lookup"><span data-stu-id="1ede2-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="1ede2-127">Sposta la trasformazione in base ai componenti orizzontali e verticali specificati.</span><span class="sxs-lookup"><span data-stu-id="1ede2-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="1ede2-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ede2-128">Properties</span></span>

<span data-ttu-id="1ede2-129">La classe **InkTransform** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1ede2-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="1ede2-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ede2-130">Property</span></span>                                     | <span data-ttu-id="1ede2-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="1ede2-131">Access type</span></span>           | <span data-ttu-id="1ede2-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ede2-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ede2-133">**Data**</span><span class="sxs-lookup"><span data-stu-id="1ede2-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="1ede2-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-134">Read/write</span></span><br/> | <span data-ttu-id="1ede2-135">Ottiene o imposta la versione di automazione dello struct di proprietà di WIN32.</span><span class="sxs-lookup"><span data-stu-id="1ede2-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="1ede2-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="1ede2-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="1ede2-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-137">Read/write</span></span><br/> | <span data-ttu-id="1ede2-138">Ottiene o imposta il numero reale che specifica l'elemento nella terza riga, prima colonna.</span><span class="sxs-lookup"><span data-stu-id="1ede2-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="1ede2-139">**eDy**</span><span class="sxs-lookup"><span data-stu-id="1ede2-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="1ede2-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-140">Read/write</span></span><br/> | <span data-ttu-id="1ede2-141">Ottiene o imposta il numero reale che specifica l'elemento nella terza riga, seconda colonna.</span><span class="sxs-lookup"><span data-stu-id="1ede2-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="1ede2-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="1ede2-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="1ede2-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-143">Read/write</span></span><br/> | <span data-ttu-id="1ede2-144">Ottiene o imposta il numero reale che specifica l'elemento nella prima riga, prima colonna.</span><span class="sxs-lookup"><span data-stu-id="1ede2-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="1ede2-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="1ede2-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="1ede2-146">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-146">Read/write</span></span><br/> | <span data-ttu-id="1ede2-147">Ottiene o imposta il numero reale che specifica l'elemento nella prima riga, seconda colonna.</span><span class="sxs-lookup"><span data-stu-id="1ede2-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="1ede2-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="1ede2-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="1ede2-149">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-149">Read/write</span></span><br/> | <span data-ttu-id="1ede2-150">Ottiene o imposta il numero reale che specifica l'elemento nella seconda riga, prima colonna.</span><span class="sxs-lookup"><span data-stu-id="1ede2-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="1ede2-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="1ede2-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="1ede2-152">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1ede2-152">Read/write</span></span><br/> | <span data-ttu-id="1ede2-153">Ottiene o imposta il numero reale che specifica l'elemento nella seconda riga, seconda colonna.</span><span class="sxs-lookup"><span data-stu-id="1ede2-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ede2-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ede2-154">Remarks</span></span>

<span data-ttu-id="1ede2-155">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="1ede2-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="1ede2-156">L'oggetto archivia solo sei dei nove numeri in una matrice 3x3 perché tutte le matrici 3x3 che rappresentano le trasformazioni affini hanno la stessa terza colonna (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1ede2-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="1ede2-157">Questo oggetto a sua volta viene usato per descrivere le operazioni di trasformazione, ad esempio lo scorrimento, il taglio, il ridimensionamento o la rotazione in un oggetto [**InkRenderer**](inkrenderer-class.md) , un oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) o una raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1ede2-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="1ede2-158">L'oggetto InkTransform è correlato alla [**struttura di**](/windows/win32/api/wingdi/ns-wingdi-xform)  .</span><span class="sxs-lookup"><span data-stu-id="1ede2-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ede2-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ede2-159">Requirements</span></span>



| <span data-ttu-id="1ede2-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ede2-160">Requirement</span></span> | <span data-ttu-id="1ede2-161">Valore</span><span class="sxs-lookup"><span data-stu-id="1ede2-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ede2-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ede2-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1ede2-163">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1ede2-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1ede2-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ede2-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1ede2-165">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1ede2-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1ede2-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ede2-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ede2-167"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1ede2-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1ede2-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ede2-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ede2-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ede2-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 

