---
description: Il \_ metodo Get ScaleX Recupera il valore in base al quale la cancellazione viene allungata orizzontalmente.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'Metodo IDxtJpeg:: get_ScaleX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328151"
---
# <a name="idxtjpegget_scalex-method"></a><span data-ttu-id="8404d-103">Metodo IDxtJpeg:: Get \_ ScaleX</span><span class="sxs-lookup"><span data-stu-id="8404d-103">IDxtJpeg::get\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="8404d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8404d-104">\[Deprecated.</span></span> <span data-ttu-id="8404d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8404d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8404d-106">Il `get_ScaleX` metodo recupera il valore in base al quale la cancellazione viene allungata orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="8404d-106">The `get_ScaleX` method retrieves the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="8404d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8404d-107">Syntax</span></span>


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8404d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8404d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8404d-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8404d-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8404d-110">Riceve il valore in base al quale la cancellazione viene allungata orizzontalmente, come percentuale della definizione di cancellazione originale.</span><span class="sxs-lookup"><span data-stu-id="8404d-110">Receives the amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="8404d-111">Ad esempio, il valore 1,0 indica l'assenza di un'estensione e 2,0 indica l'estensione del 200%.</span><span class="sxs-lookup"><span data-stu-id="8404d-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8404d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8404d-112">Return value</span></span>

<span data-ttu-id="8404d-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8404d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8404d-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8404d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8404d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8404d-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8404d-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8404d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8404d-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8404d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8404d-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8404d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8404d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8404d-119">Requirements</span></span>



| <span data-ttu-id="8404d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8404d-120">Requirement</span></span> | <span data-ttu-id="8404d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8404d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8404d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8404d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8404d-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8404d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8404d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="8404d-124">Library</span></span><br/> | <dl> <span data-ttu-id="8404d-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8404d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8404d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8404d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8404d-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="8404d-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




