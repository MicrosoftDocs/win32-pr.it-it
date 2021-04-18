---
description: Il metodo EffectGetCount Recupera il numero di effetti su questo oggetto.
ms.assetid: 6cf3b5b1-f38f-4ee1-8567-3c55f4f89cbb
title: 'Metodo IAMTimelineEffectable:: EffectGetCount (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 247af794c2336c80e251d1a970e1d90925d4c53c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333698"
---
# <a name="iamtimelineeffectableeffectgetcount-method"></a><span data-ttu-id="345a7-103">Metodo IAMTimelineEffectable:: EffectGetCount</span><span class="sxs-lookup"><span data-stu-id="345a7-103">IAMTimelineEffectable::EffectGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="345a7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="345a7-104">\[Deprecated.</span></span> <span data-ttu-id="345a7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="345a7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="345a7-106">Il `EffectGetCount` metodo recupera il numero di effetti su questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="345a7-106">The `EffectGetCount` method retrieves the number of effects on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="345a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="345a7-107">Syntax</span></span>


```C++
HRESULT EffectGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="345a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="345a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="345a7-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="345a7-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="345a7-110">Riceve il numero di effetti.</span><span class="sxs-lookup"><span data-stu-id="345a7-110">Receives the number of effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="345a7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="345a7-111">Return value</span></span>

<span data-ttu-id="345a7-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="345a7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="345a7-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="345a7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="345a7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="345a7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="345a7-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="345a7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="345a7-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="345a7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="345a7-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="345a7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="345a7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="345a7-118">Requirements</span></span>



| <span data-ttu-id="345a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="345a7-119">Requirement</span></span> | <span data-ttu-id="345a7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="345a7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="345a7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="345a7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="345a7-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="345a7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="345a7-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="345a7-123">Library</span></span><br/> | <dl> <span data-ttu-id="345a7-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="345a7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345a7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="345a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345a7-126">**Interfaccia IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="345a7-126">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="345a7-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="345a7-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




