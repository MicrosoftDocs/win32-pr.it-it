---
description: Il metodo SetSubObjectGUID specifica il GUID dell'oggetto SubObject associato a questo oggetto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'Metodo IAMTimelineObj:: SetSubObjectGUID (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330803"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="31ea8-103">Metodo IAMTimelineObj:: SetSubObjectGUID</span><span class="sxs-lookup"><span data-stu-id="31ea8-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="31ea8-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="31ea8-104">\[Deprecated.</span></span> <span data-ttu-id="31ea8-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="31ea8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="31ea8-106">Il `SetSubObjectGUID` metodo specifica il GUID dell'oggetto SubObject associato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="31ea8-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ea8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31ea8-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="31ea8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="31ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ea8-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="31ea8-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="31ea8-110">GUID dell'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="31ea8-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ea8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31ea8-111">Return value</span></span>

<span data-ttu-id="31ea8-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="31ea8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31ea8-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31ea8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ea8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="31ea8-114">Remarks</span></span>

<span data-ttu-id="31ea8-115">Il motore di rendering crea un'istanza dell'oggetto sottooggetto in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="31ea8-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="31ea8-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="31ea8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="31ea8-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="31ea8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="31ea8-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="31ea8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31ea8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31ea8-119">Requirements</span></span>



| <span data-ttu-id="31ea8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="31ea8-120">Requirement</span></span> | <span data-ttu-id="31ea8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="31ea8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ea8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31ea8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="31ea8-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ea8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="31ea8-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="31ea8-124">Library</span></span><br/> | <dl> <span data-ttu-id="31ea8-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ea8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31ea8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31ea8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ea8-127">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="31ea8-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="31ea8-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="31ea8-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




