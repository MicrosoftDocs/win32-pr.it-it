---
description: L'interfaccia IDxtCompositor imposta le proprietà nella transizione del Compositor. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione del Compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interfaccia IDxtCompositor (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331513"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="3d131-103">Interfaccia IDxtCompositor</span><span class="sxs-lookup"><span data-stu-id="3d131-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="3d131-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3d131-104">\[Deprecated.</span></span> <span data-ttu-id="3d131-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3d131-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3d131-106">L' `IDxtCompositor` interfaccia imposta le proprietà nella transizione del [compositor](compositor-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="3d131-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="3d131-107">Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione del Compositor.</span><span class="sxs-lookup"><span data-stu-id="3d131-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="3d131-108">Non è necessario che le applicazioni DES usino questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3d131-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="3d131-109">Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="3d131-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="3d131-110">La transizione del Compositor compone un'immagine di primo piano su un'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="3d131-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="3d131-111">Il *rettangolo di origine* definisce la sezione dell'immagine in primo piano composta.</span><span class="sxs-lookup"><span data-stu-id="3d131-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="3d131-112">Il *rettangolo di destinazione* definisce la sezione dell'immagine di sfondo che riceve l'immagine in primo piano.</span><span class="sxs-lookup"><span data-stu-id="3d131-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="3d131-113">Il diagramma seguente illustra questi rettangoli.</span><span class="sxs-lookup"><span data-stu-id="3d131-113">The following diagram illustrates these rectangles.</span></span>

![Proprietà di transizione del Compositor](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="3d131-115">Membri</span><span class="sxs-lookup"><span data-stu-id="3d131-115">Members</span></span>

<span data-ttu-id="3d131-116">L'interfaccia **IDxtCompositor** eredita da **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="3d131-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="3d131-117">**IDxtCompositor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3d131-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="3d131-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="3d131-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3d131-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="3d131-119">Methods</span></span>

<span data-ttu-id="3d131-120">L'interfaccia **IDxtCompositor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3d131-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="3d131-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="3d131-121">Method</span></span>                                                   | <span data-ttu-id="3d131-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d131-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="3d131-123">**Ottieni \_ altezza**</span><span class="sxs-lookup"><span data-stu-id="3d131-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="3d131-124">Recupera l'altezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="3d131-125">**ottenere \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="3d131-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="3d131-126">Recupera l'offset orizzontale del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="3d131-127">**Ottieni \_ offset**</span><span class="sxs-lookup"><span data-stu-id="3d131-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="3d131-128">Recupera l'offset verticale del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="3d131-129">**ottenere \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="3d131-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="3d131-130">Recupera l'altezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="3d131-131">**ottenere \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="3d131-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="3d131-132">Recupera l'offset orizzontale del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="3d131-133">**ottenere \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="3d131-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="3d131-134">Recupera l'offset verticale del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="3d131-135">**ottenere \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="3d131-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="3d131-136">Recupera la larghezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="3d131-137">**Ottieni \_ larghezza**</span><span class="sxs-lookup"><span data-stu-id="3d131-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="3d131-138">Recupera la larghezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="3d131-139">**\_altezza put**</span><span class="sxs-lookup"><span data-stu-id="3d131-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="3d131-140">Specifica l'altezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="3d131-141">**Inserisci \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="3d131-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="3d131-142">Specifica l'offset orizzontale del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="3d131-143">**Inserisci \_ offset**</span><span class="sxs-lookup"><span data-stu-id="3d131-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="3d131-144">Specifica l'offset verticale del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="3d131-145">**Inserisci \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="3d131-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="3d131-146">Specifica l'altezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="3d131-147">**Inserisci \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="3d131-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="3d131-148">Specifica l'offset orizzontale del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="3d131-149">**Inserisci \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="3d131-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="3d131-150">Specifica l'offset verticale del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="3d131-151">**Inserisci \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="3d131-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="3d131-152">Specifica la larghezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3d131-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="3d131-153">**Inserisci \_ larghezza**</span><span class="sxs-lookup"><span data-stu-id="3d131-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="3d131-154">Specifica la larghezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d131-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="3d131-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d131-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3d131-156">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="3d131-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3d131-157">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3d131-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3d131-158">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3d131-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d131-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d131-159">Requirements</span></span>



| <span data-ttu-id="3d131-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d131-160">Requirement</span></span> | <span data-ttu-id="3d131-161">Valore</span><span class="sxs-lookup"><span data-stu-id="3d131-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d131-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d131-162">Header</span></span><br/>  | <dl> <span data-ttu-id="3d131-163"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d131-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3d131-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d131-164">Library</span></span><br/> | <dl> <span data-ttu-id="3d131-165"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d131-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




