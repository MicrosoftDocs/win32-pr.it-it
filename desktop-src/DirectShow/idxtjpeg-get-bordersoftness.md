---
description: Il \_ metodo Get BorderSoftness recupera la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.
ms.assetid: f5648cce-e44c-4ed6-8254-6511cd600629
title: 'Metodo IDxtJpeg:: get_BorderSoftness (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 968dbef4a87a7b88e16321693350d35d08225c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326274"
---
# <a name="idxtjpegget_bordersoftness-method"></a><span data-ttu-id="f15cb-103">Metodo IDxtJpeg:: Get \_ BorderSoftness</span><span class="sxs-lookup"><span data-stu-id="f15cb-103">IDxtJpeg::get\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="f15cb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f15cb-104">\[Deprecated.</span></span> <span data-ttu-id="f15cb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f15cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f15cb-106">Il `get_BorderSoftness` metodo recupera la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="f15cb-106">The `get_BorderSoftness` method retrieves the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15cb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f15cb-107">Syntax</span></span>


```C++
HRESULT get_BorderSoftness(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f15cb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f15cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15cb-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f15cb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f15cb-110">Riceve la larghezza, in pixel, dell'area sfocata.</span><span class="sxs-lookup"><span data-stu-id="f15cb-110">Receives the width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15cb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f15cb-111">Return value</span></span>

<span data-ttu-id="f15cb-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f15cb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f15cb-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f15cb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15cb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f15cb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f15cb-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f15cb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f15cb-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f15cb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f15cb-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f15cb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f15cb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f15cb-118">Requirements</span></span>



| <span data-ttu-id="f15cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15cb-119">Requirement</span></span> | <span data-ttu-id="f15cb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f15cb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15cb-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f15cb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f15cb-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15cb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f15cb-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f15cb-123">Library</span></span><br/> | <dl> <span data-ttu-id="f15cb-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f15cb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15cb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f15cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15cb-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="f15cb-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




