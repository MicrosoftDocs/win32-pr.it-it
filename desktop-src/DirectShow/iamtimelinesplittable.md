---
description: L'interfaccia IAMTimelineSplittable suddivide un oggetto Timeline in servizi di modifica DirectShow (DES). Le origini, gli effetti, le transizioni e le tracce implementano questa interfaccia.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interfaccia IAMTimelineSplittable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324265"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="061a6-104">Interfaccia IAMTimelineSplittable</span><span class="sxs-lookup"><span data-stu-id="061a6-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="061a6-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="061a6-105">\[Deprecated.</span></span> <span data-ttu-id="061a6-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="061a6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="061a6-107">L' `IAMTimelineSplittable` interfaccia suddivide un oggetto sequenza temporale in [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="061a6-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="061a6-108">Le origini, gli effetti, le transizioni e le tracce implementano questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="061a6-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="061a6-109">Membri</span><span class="sxs-lookup"><span data-stu-id="061a6-109">Members</span></span>

<span data-ttu-id="061a6-110">L'interfaccia **IAMTimelineSplittable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="061a6-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="061a6-111">**IAMTimelineSplittable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="061a6-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="061a6-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="061a6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="061a6-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="061a6-113">Methods</span></span>

<span data-ttu-id="061a6-114">L'interfaccia **IAMTimelineSplittable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="061a6-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="061a6-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="061a6-115">Method</span></span>                                             | <span data-ttu-id="061a6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="061a6-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="061a6-117">**SplitAt**</span><span class="sxs-lookup"><span data-stu-id="061a6-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="061a6-118">Suddivide l'oggetto all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="061a6-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="061a6-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="061a6-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="061a6-120">Suddivide l'oggetto all'ora specificata, specificato come valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="061a6-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="061a6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="061a6-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="061a6-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="061a6-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="061a6-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="061a6-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="061a6-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="061a6-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="061a6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="061a6-125">Requirements</span></span>



| <span data-ttu-id="061a6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="061a6-126">Requirement</span></span> | <span data-ttu-id="061a6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="061a6-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="061a6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="061a6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="061a6-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="061a6-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="061a6-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="061a6-130">Library</span></span><br/> | <dl> <span data-ttu-id="061a6-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="061a6-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
