---
description: Il \_ metodo Put MaskNum specifica il codice di cancellazione SMPTE della cancellazione.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: 'IDxtJpeg: metodo:p ut_MaskNum (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327329"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="06244-103">IDxtJpeg::p UT \_ MaskNum metodo</span><span class="sxs-lookup"><span data-stu-id="06244-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="06244-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="06244-104">\[Deprecated.</span></span> <span data-ttu-id="06244-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="06244-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="06244-106">Il `put_MaskNum` metodo specifica il codice di cancellazione SMPTE della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="06244-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="06244-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06244-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="06244-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06244-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06244-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06244-110">Specifica il codice di cancellazione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="06244-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="06244-111">Per un elenco delle salviette SMPTE supportate, vedere la pagina relativa alla [transizione di cancellazione SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="06244-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06244-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06244-112">Return value</span></span>

<span data-ttu-id="06244-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="06244-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06244-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06244-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06244-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="06244-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06244-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="06244-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="06244-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="06244-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="06244-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="06244-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06244-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06244-119">Requirements</span></span>



| <span data-ttu-id="06244-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="06244-120">Requirement</span></span> | <span data-ttu-id="06244-121">Valore</span><span class="sxs-lookup"><span data-stu-id="06244-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06244-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06244-122">Header</span></span><br/>  | <dl> <span data-ttu-id="06244-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06244-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="06244-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="06244-124">Library</span></span><br/> | <dl> <span data-ttu-id="06244-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06244-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06244-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06244-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06244-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="06244-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




