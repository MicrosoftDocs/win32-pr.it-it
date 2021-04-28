---
title: Metodo IEnumBackgroundCopyFiles Reset (Deliveryoptimization.h)
description: "Metodo IEnumBackgroundCopyFiles::Reset: reimposta la sequenza di enumerazione all'inizio."
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset (metodo)
- Metodo Reset, interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, metodo Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6800095d0a6f20ef8b632830a224d4da27356bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105489"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="9470f-106">Metodo IEnumBackgroundCopyFiles::Reset</span><span class="sxs-lookup"><span data-stu-id="9470f-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="9470f-107">Riporta all'inizio la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9470f-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="9470f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9470f-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="9470f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9470f-109">Parameters</span></span>

<span data-ttu-id="9470f-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9470f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9470f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9470f-111">Return value</span></span>

<span data-ttu-id="9470f-112">Questo metodo **restituisce** S_OK in caso di esito positivo o uno dei valori **HRESULT** COM standard in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="9470f-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9470f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9470f-113">Requirements</span></span>



| <span data-ttu-id="9470f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9470f-114">Requirement</span></span> | <span data-ttu-id="9470f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9470f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9470f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9470f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9470f-117">Windows 10, solo app desktop versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="9470f-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9470f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9470f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9470f-119">Windows Server, solo app desktop versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="9470f-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9470f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9470f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9470f-121"><dt>Deliveryoptimization.h</dt></span><span class="sxs-lookup"><span data-stu-id="9470f-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9470f-122">Idl</span><span class="sxs-lookup"><span data-stu-id="9470f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9470f-123"><dt>DeliveryOptimization.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9470f-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9470f-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="9470f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9470f-125"><dt>Dosvc.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9470f-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9470f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9470f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9470f-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9470f-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9470f-128">IID</span><span class="sxs-lookup"><span data-stu-id="9470f-128">IID</span></span><br/>                      | <span data-ttu-id="9470f-129">IID_IEnumBackgroundCopyFiles è definito come CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="9470f-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="9470f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9470f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9470f-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="9470f-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





