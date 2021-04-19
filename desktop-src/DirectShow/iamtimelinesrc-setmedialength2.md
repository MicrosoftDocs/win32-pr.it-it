---
description: 'Il metodo SetMediaLength2 specifica la durata del file di origine. Questo metodo è equivalente a IAMTimelineSrc:: SetMediaLength, ma accetta un valore REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'Metodo IAMTimelineSrc:: SetMediaLength2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330182"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="b5f48-104">Metodo IAMTimelineSrc:: SetMediaLength2</span><span class="sxs-lookup"><span data-stu-id="b5f48-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="b5f48-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b5f48-105">\[Deprecated.</span></span> <span data-ttu-id="b5f48-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b5f48-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b5f48-107">Il `SetMediaLength2` metodo specifica la durata del file di origine.</span><span class="sxs-lookup"><span data-stu-id="b5f48-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="b5f48-108">Questo metodo è equivalente a [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b5f48-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f48-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5f48-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="b5f48-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5f48-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f48-111">*Length*</span><span class="sxs-lookup"><span data-stu-id="b5f48-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f48-112">Lunghezza del supporto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="b5f48-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f48-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5f48-113">Return value</span></span>

<span data-ttu-id="b5f48-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b5f48-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5f48-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5f48-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f48-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5f48-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5f48-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b5f48-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b5f48-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b5f48-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b5f48-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b5f48-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5f48-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5f48-120">Requirements</span></span>



| <span data-ttu-id="b5f48-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f48-121">Requirement</span></span> | <span data-ttu-id="b5f48-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b5f48-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f48-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5f48-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b5f48-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f48-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b5f48-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5f48-125">Library</span></span><br/> | <dl> <span data-ttu-id="b5f48-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5f48-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f48-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5f48-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f48-128">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="b5f48-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="b5f48-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b5f48-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




