---
description: Il \_ metodo Put BorderColor specifica il colore del bordo intorno ai bordi del pattern di cancellazione.
ms.assetid: d6a49956-8fc9-4ba2-8485-a49175da3cf7
title: 'IDxtJpeg: metodo:p ut_BorderColor (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faacc76eaa120467aa6cfb6c318aac0d9baec334
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325919"
---
# <a name="idxtjpegput_bordercolor-method"></a><span data-ttu-id="09acc-103">IDxtJpeg: metodo:p UT \_ BorderColor</span><span class="sxs-lookup"><span data-stu-id="09acc-103">IDxtJpeg::put\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="09acc-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="09acc-104">\[Deprecated.</span></span> <span data-ttu-id="09acc-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09acc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="09acc-106">Il `put_BorderColor` metodo specifica il colore del bordo intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="09acc-106">The `put_BorderColor` method specifies the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="09acc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09acc-107">Syntax</span></span>


```C++
HRESULT put_BorderColor(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="09acc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09acc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09acc-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09acc-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09acc-110">Specifica il colore come numero esadecimale con formato 0xRRGGBB, dove RR è il valore rosso, GG è il valore verde e BB è il valore blu.</span><span class="sxs-lookup"><span data-stu-id="09acc-110">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09acc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09acc-111">Return value</span></span>

<span data-ttu-id="09acc-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09acc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09acc-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09acc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09acc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="09acc-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="09acc-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="09acc-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="09acc-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="09acc-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="09acc-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="09acc-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09acc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09acc-118">Requirements</span></span>



| <span data-ttu-id="09acc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="09acc-119">Requirement</span></span> | <span data-ttu-id="09acc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="09acc-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09acc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09acc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="09acc-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="09acc-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="09acc-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="09acc-123">Library</span></span><br/> | <dl> <span data-ttu-id="09acc-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09acc-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09acc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09acc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09acc-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="09acc-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




