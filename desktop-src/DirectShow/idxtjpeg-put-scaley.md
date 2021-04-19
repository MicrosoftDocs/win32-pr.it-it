---
description: Il \_ metodo Put ScaleY specifica la quantità in base alla quale la cancellazione viene allungata verticalmente.
ms.assetid: 1dd84540-b249-482c-9cb7-aab8c7dc4d25
title: 'IDxtJpeg: metodo:p ut_ScaleY (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65a8b736dc66ec9dad20b1e261ecd7b0c4556774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326546"
---
# <a name="idxtjpegput_scaley-method"></a><span data-ttu-id="15588-103">IDxtJpeg::p \_ metodo di scalabilità UT</span><span class="sxs-lookup"><span data-stu-id="15588-103">IDxtJpeg::put\_ScaleY method</span></span>

> [!Note]  
> <span data-ttu-id="15588-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="15588-104">\[Deprecated.</span></span> <span data-ttu-id="15588-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15588-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15588-106">Il `put_ScaleY` metodo specifica la quantità in base alla quale la cancellazione viene allungata verticalmente.</span><span class="sxs-lookup"><span data-stu-id="15588-106">The `put_ScaleY` method specifies the amount by which the wipe is stretched vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="15588-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15588-107">Syntax</span></span>


```C++
HRESULT put_ScaleY(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="15588-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15588-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15588-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15588-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15588-110">Importo in base al quale la cancellazione viene allungata verticalmente, come percentuale della definizione di cancellazione originale.</span><span class="sxs-lookup"><span data-stu-id="15588-110">The amount by which the wipe is stretched vertically, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="15588-111">Ad esempio, il valore 1,0 indica l'assenza di un'estensione e 2,0 indica l'estensione del 200%.</span><span class="sxs-lookup"><span data-stu-id="15588-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15588-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15588-112">Return value</span></span>

<span data-ttu-id="15588-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15588-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15588-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15588-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="15588-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="15588-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="15588-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="15588-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="15588-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="15588-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="15588-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="15588-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15588-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15588-119">Requirements</span></span>



| <span data-ttu-id="15588-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="15588-120">Requirement</span></span> | <span data-ttu-id="15588-121">Valore</span><span class="sxs-lookup"><span data-stu-id="15588-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15588-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15588-122">Header</span></span><br/>  | <dl> <span data-ttu-id="15588-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="15588-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="15588-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="15588-124">Library</span></span><br/> | <dl> <span data-ttu-id="15588-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15588-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15588-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15588-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15588-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="15588-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




