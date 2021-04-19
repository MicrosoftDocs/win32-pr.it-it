---
description: Il \_ metodo Put maskName specifica il nome di un file JPEG da usare come maschera di cancellazione.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg: metodo:p ut_MaskName (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329251"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="e22c3-103">IDxtJpeg::p UT \_ maskName metodo</span><span class="sxs-lookup"><span data-stu-id="e22c3-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="e22c3-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e22c3-104">\[Deprecated.</span></span> <span data-ttu-id="e22c3-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e22c3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e22c3-106">Il `put_MaskName` metodo specifica il nome di un file JPEG da usare come maschera di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="e22c3-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="e22c3-107">Questa maschera verrà utilizzata al posto di una delle maschere di cancellazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="e22c3-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="e22c3-108">Il file deve contenere una sfumatura monocromatica a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="e22c3-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="e22c3-109">La sfumatura viene utilizzata come maschera per definire la progressione della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="e22c3-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22c3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e22c3-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e22c3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e22c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22c3-112">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e22c3-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e22c3-113">Specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="e22c3-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22c3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e22c3-114">Return value</span></span>

<span data-ttu-id="e22c3-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e22c3-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e22c3-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e22c3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e22c3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e22c3-117">Remarks</span></span>

<span data-ttu-id="e22c3-118">Per ripristinare una maschera predefinita, impostare la proprietà **MaskNum** .</span><span class="sxs-lookup"><span data-stu-id="e22c3-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="e22c3-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e22c3-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e22c3-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e22c3-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e22c3-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e22c3-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e22c3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e22c3-122">Requirements</span></span>



| <span data-ttu-id="e22c3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e22c3-123">Requirement</span></span> | <span data-ttu-id="e22c3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e22c3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e22c3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e22c3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e22c3-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e22c3-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e22c3-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="e22c3-127">Library</span></span><br/> | <dl> <span data-ttu-id="e22c3-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e22c3-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22c3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e22c3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22c3-130">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="e22c3-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="e22c3-131">**IDxtJpeg::p UT \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="e22c3-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




