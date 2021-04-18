---
description: Il \_ metodo Put BorderSoftness specifica la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: 'IDxtJpeg: metodo:p ut_BorderSoftness (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332190"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="1f6da-103">IDxtJpeg::p UT \_ BorderSoftness metodo</span><span class="sxs-lookup"><span data-stu-id="1f6da-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="1f6da-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1f6da-104">\[Deprecated.</span></span> <span data-ttu-id="1f6da-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1f6da-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1f6da-106">Il `put_BorderSoftness` metodo specifica la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="1f6da-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f6da-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="1f6da-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f6da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f6da-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f6da-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6da-110">Larghezza, in pixel, dell'area sfocata.</span><span class="sxs-lookup"><span data-stu-id="1f6da-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f6da-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f6da-111">Return value</span></span>

<span data-ttu-id="1f6da-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1f6da-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f6da-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f6da-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6da-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f6da-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f6da-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="1f6da-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1f6da-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1f6da-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1f6da-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1f6da-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f6da-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f6da-118">Requirements</span></span>



| <span data-ttu-id="1f6da-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f6da-119">Requirement</span></span> | <span data-ttu-id="1f6da-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1f6da-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6da-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f6da-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1f6da-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f6da-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1f6da-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f6da-123">Library</span></span><br/> | <dl> <span data-ttu-id="1f6da-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f6da-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6da-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f6da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6da-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="1f6da-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




