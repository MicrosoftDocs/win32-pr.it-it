---
description: Il metodo TransGetCount Recupera il numero di transizioni in questo oggetto.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: 'Metodo IAMTimelineTransable:: TransGetCount (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81b5fc6301b319b8716a6db25fce2b1e5c2d4961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332961"
---
# <a name="iamtimelinetransabletransgetcount-method"></a><span data-ttu-id="1d49a-103">Metodo IAMTimelineTransable:: TransGetCount</span><span class="sxs-lookup"><span data-stu-id="1d49a-103">IAMTimelineTransable::TransGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="1d49a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1d49a-104">\[Deprecated.</span></span> <span data-ttu-id="1d49a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d49a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d49a-106">Il `TransGetCount` metodo recupera il numero di transizioni in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="1d49a-106">The `TransGetCount` method retrieves the number of transitions on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d49a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d49a-107">Syntax</span></span>


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="1d49a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d49a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d49a-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="1d49a-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="1d49a-110">Riceve il numero di transizioni.</span><span class="sxs-lookup"><span data-stu-id="1d49a-110">Receives the number of transitions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d49a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d49a-111">Return value</span></span>

<span data-ttu-id="1d49a-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1d49a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d49a-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d49a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d49a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d49a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d49a-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="1d49a-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d49a-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d49a-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1d49a-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1d49a-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d49a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d49a-118">Requirements</span></span>



| <span data-ttu-id="1d49a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d49a-119">Requirement</span></span> | <span data-ttu-id="1d49a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1d49a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d49a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d49a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1d49a-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d49a-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1d49a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d49a-123">Library</span></span><br/> | <dl> <span data-ttu-id="1d49a-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d49a-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d49a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d49a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d49a-126">**Interfaccia IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="1d49a-126">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="1d49a-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1d49a-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




