---
title: Metodo Reset IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Riporta all'inizio la sequenza di enumerazione.
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
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873613"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="582b7-106">Metodo IEnumBackgroundCopyFiles:: Reset</span><span class="sxs-lookup"><span data-stu-id="582b7-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="582b7-107">Riporta all'inizio la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="582b7-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="582b7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="582b7-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="582b7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="582b7-109">Parameters</span></span>

<span data-ttu-id="582b7-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="582b7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="582b7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="582b7-111">Return value</span></span>

<span data-ttu-id="582b7-112">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="582b7-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="582b7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="582b7-113">Requirements</span></span>



| <span data-ttu-id="582b7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="582b7-114">Requirement</span></span> | <span data-ttu-id="582b7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="582b7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582b7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="582b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="582b7-117">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="582b7-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="582b7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="582b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="582b7-119">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="582b7-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="582b7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="582b7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="582b7-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="582b7-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="582b7-122">IDL</span><span class="sxs-lookup"><span data-stu-id="582b7-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="582b7-123"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="582b7-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="582b7-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="582b7-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="582b7-125"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="582b7-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="582b7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="582b7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="582b7-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="582b7-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="582b7-128">IID</span><span class="sxs-lookup"><span data-stu-id="582b7-128">IID</span></span><br/>                      | <span data-ttu-id="582b7-129">IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="582b7-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="582b7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="582b7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="582b7-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="582b7-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





