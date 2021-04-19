---
description: L'interfaccia IDxtJpeg imposta le proprietà della transizione di cancellazione SMPTE. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione di cancellazione SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interfaccia IDxtJpeg (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326923"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="57b66-103">Interfaccia IDxtJpeg</span><span class="sxs-lookup"><span data-stu-id="57b66-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="57b66-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="57b66-104">\[Deprecated.</span></span> <span data-ttu-id="57b66-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57b66-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="57b66-106">L' `IDxtJpeg` interfaccia imposta le proprietà della transizione di [cancellazione SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="57b66-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="57b66-107">Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione di cancellazione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="57b66-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="57b66-108">Non è necessario che le applicazioni DES usino questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="57b66-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="57b66-109">Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="57b66-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="57b66-110">Membri</span><span class="sxs-lookup"><span data-stu-id="57b66-110">Members</span></span>

<span data-ttu-id="57b66-111">L'interfaccia **IDxtJpeg** eredita da **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="57b66-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="57b66-112">**IDxtJpeg** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="57b66-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="57b66-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="57b66-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="57b66-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="57b66-114">Methods</span></span>

<span data-ttu-id="57b66-115">L'interfaccia **IDxtJpeg** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="57b66-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="57b66-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="57b66-116">Method</span></span>                                                     | <span data-ttu-id="57b66-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57b66-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57b66-118">**ApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="57b66-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="57b66-119">Applica le proprietà che sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="57b66-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="57b66-120">**ottenere \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="57b66-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="57b66-121">Recupera il colore del bordo intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="57b66-122">**ottenere \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="57b66-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="57b66-123">Recupera la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="57b66-124">**ottenere \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="57b66-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="57b66-125">Recupera la larghezza del bordo solido lungo i bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="57b66-126">**Ottieni \_ maskName**</span><span class="sxs-lookup"><span data-stu-id="57b66-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="57b66-127">Recupera il nome di un file JPEG da utilizzare come maschera di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="57b66-128">**ottenere \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="57b66-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="57b66-129">Recupera il codice di cancellazione SMPTE della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="57b66-130">**ottenere \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="57b66-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="57b66-131">Recupera l'offset orizzontale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="57b66-132">**Ottieni \_ offset**</span><span class="sxs-lookup"><span data-stu-id="57b66-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="57b66-133">Recupera l'offset verticale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="57b66-134">**ottenere \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="57b66-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="57b66-135">Recupera il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="57b66-136">**ottenere la \_ replica**</span><span class="sxs-lookup"><span data-stu-id="57b66-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="57b66-137">Recupera il numero di volte in cui il modello di cancellazione viene replicato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="57b66-138">**Ottieni \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="57b66-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="57b66-139">Recupera il valore in base al quale la cancellazione viene allungata orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="57b66-140">**Ottieni \_ scalabilità**</span><span class="sxs-lookup"><span data-stu-id="57b66-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="57b66-141">Recupera il valore in base al quale la cancellazione viene allungata verticalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="57b66-142">**LoadDefSettings**</span><span class="sxs-lookup"><span data-stu-id="57b66-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="57b66-143">Ripristina le impostazioni predefinite della transizione di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="57b66-144">**Inserisci \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="57b66-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="57b66-145">Specifica il colore del bordo intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="57b66-146">**Inserisci \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="57b66-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="57b66-147">Specifica la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="57b66-148">**Inserisci \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="57b66-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="57b66-149">Specifica lo spessore del bordo a tinta unita lungo i bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="57b66-150">**Inserisci \_ maskName**</span><span class="sxs-lookup"><span data-stu-id="57b66-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="57b66-151">Specifica il nome di un file JPEG da usare come maschera di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="57b66-152">**Inserisci \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="57b66-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="57b66-153">Specifica il codice di cancellazione SMPTE della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="57b66-154">**Inserisci \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="57b66-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="57b66-155">Specifica l'offset orizzontale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="57b66-156">**Inserisci \_ offset**</span><span class="sxs-lookup"><span data-stu-id="57b66-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="57b66-157">Specifica l'offset verticale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="57b66-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="57b66-158">**Inserisci \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="57b66-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="57b66-159">Specifica il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="57b66-160">**Inserisci \_ replica**</span><span class="sxs-lookup"><span data-stu-id="57b66-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="57b66-161">Specifica il numero di volte in cui il modello di cancellazione viene replicato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="57b66-162">**Inserisci \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="57b66-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="57b66-163">Specifica la quantità in base alla quale la cancellazione viene allungata orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="57b66-164">**\_scalabilità orizzontale**</span><span class="sxs-lookup"><span data-stu-id="57b66-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="57b66-165">Specifica la quantità in base alla quale la cancellazione viene allungata verticalmente.</span><span class="sxs-lookup"><span data-stu-id="57b66-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="57b66-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="57b66-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57b66-167">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="57b66-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="57b66-168">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="57b66-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="57b66-169">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="57b66-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57b66-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57b66-170">Requirements</span></span>



| <span data-ttu-id="57b66-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b66-171">Requirement</span></span> | <span data-ttu-id="57b66-172">Valore</span><span class="sxs-lookup"><span data-stu-id="57b66-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57b66-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57b66-173">Header</span></span><br/>  | <dl> <span data-ttu-id="57b66-174"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57b66-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="57b66-175">Libreria</span><span class="sxs-lookup"><span data-stu-id="57b66-175">Library</span></span><br/> | <dl> <span data-ttu-id="57b66-176"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57b66-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




