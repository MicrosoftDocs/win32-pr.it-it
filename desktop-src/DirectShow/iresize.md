---
description: "L'interfaccia IResize deve essere supportata da qualsiasi filtro di ridimensionamento video personalizzato per i servizi di modifica DirectShow (DES). Per impostare un filtro Resizer personalizzato, chiamare il metodo IRenderEngine2:: SetResizerGUID sul motore di rendering."
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interfaccia IResize (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325298"
---
# <a name="iresize-interface"></a><span data-ttu-id="dddd5-104">Interfaccia IResize</span><span class="sxs-lookup"><span data-stu-id="dddd5-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="dddd5-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dddd5-105">\[Deprecated.</span></span> <span data-ttu-id="dddd5-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dddd5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dddd5-107">L' `IResize` interfaccia deve essere supportata da qualsiasi filtro di ridimensionamento video personalizzato per i servizi di modifica DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="dddd5-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="dddd5-108">Per impostare un filtro Resizer personalizzato, chiamare il metodo [**IRenderEngine2:: SetResizerGUID**](irenderengine2-setresizerguid.md) sul motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="dddd5-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="dddd5-109">Membri</span><span class="sxs-lookup"><span data-stu-id="dddd5-109">Members</span></span>

<span data-ttu-id="dddd5-110">L'interfaccia **IResize** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dddd5-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dddd5-111">**IResize** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dddd5-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="dddd5-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="dddd5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dddd5-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="dddd5-113">Methods</span></span>

<span data-ttu-id="dddd5-114">L'interfaccia **IResize** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="dddd5-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="dddd5-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="dddd5-115">Method</span></span>                                          | <span data-ttu-id="dddd5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dddd5-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="dddd5-117">**ottenere \_ InputSize**</span><span class="sxs-lookup"><span data-stu-id="dddd5-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="dddd5-118">Restituisce le dimensioni di input correnti del filtro Resizer.</span><span class="sxs-lookup"><span data-stu-id="dddd5-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="dddd5-119">**ottenere \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="dddd5-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="dddd5-120">Restituisce il tipo di supporto di output del filtro di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="dddd5-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="dddd5-121">**Ottieni \_ dimensioni**</span><span class="sxs-lookup"><span data-stu-id="dddd5-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="dddd5-122">Restituisce le dimensioni di output e la modalità di estensione correnti.</span><span class="sxs-lookup"><span data-stu-id="dddd5-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="dddd5-123">**Inserisci \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="dddd5-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="dddd5-124">Imposta il tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="dddd5-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="dddd5-125">**\_dimensioni put**</span><span class="sxs-lookup"><span data-stu-id="dddd5-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="dddd5-126">Imposta le dimensioni di output e la modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="dddd5-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="dddd5-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="dddd5-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dddd5-128">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="dddd5-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dddd5-129">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dddd5-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dddd5-130">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dddd5-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dddd5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dddd5-131">Requirements</span></span>



| <span data-ttu-id="dddd5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dddd5-132">Requirement</span></span> | <span data-ttu-id="dddd5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="dddd5-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dddd5-134">Versione</span><span class="sxs-lookup"><span data-stu-id="dddd5-134">Version</span></span><br/> | <span data-ttu-id="dddd5-135">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dddd5-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="dddd5-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dddd5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="dddd5-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dddd5-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dddd5-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="dddd5-138">Library</span></span><br/> | <dl> <span data-ttu-id="dddd5-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dddd5-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dddd5-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dddd5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dddd5-141">Creazione di una ridisposizione video personalizzata</span><span class="sxs-lookup"><span data-stu-id="dddd5-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
