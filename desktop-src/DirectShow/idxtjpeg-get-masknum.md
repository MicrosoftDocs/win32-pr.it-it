---
description: Il \_ metodo Get MaskNum Recupera il codice di cancellazione SMPTE della cancellazione.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Metodo IDxtJpeg:: get_MaskNum (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 869809fdea6e1c329088abca50a1670239554327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326779"
---
# <a name="idxtjpegget_masknum-method"></a><span data-ttu-id="6973b-103">Metodo IDxtJpeg:: Get \_ MaskNum</span><span class="sxs-lookup"><span data-stu-id="6973b-103">IDxtJpeg::get\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="6973b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6973b-104">\[Deprecated.</span></span> <span data-ttu-id="6973b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6973b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6973b-106">Il `get_MaskNum` metodo recupera il codice di cancellazione SMPTE della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="6973b-106">The `get_MaskNum` method retrieves the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="6973b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6973b-107">Syntax</span></span>


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6973b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6973b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6973b-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6973b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6973b-110">Riceve il codice di cancellazione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6973b-110">Receives the SMPTE wipe code.</span></span> <span data-ttu-id="6973b-111">Per un elenco delle salviette SMPTE supportate, vedere la pagina relativa alla [transizione di cancellazione SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="6973b-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6973b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6973b-112">Return value</span></span>

<span data-ttu-id="6973b-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6973b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6973b-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6973b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6973b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6973b-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6973b-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6973b-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6973b-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6973b-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6973b-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6973b-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6973b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6973b-119">Requirements</span></span>



| <span data-ttu-id="6973b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6973b-120">Requirement</span></span> | <span data-ttu-id="6973b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6973b-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6973b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6973b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6973b-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6973b-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6973b-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="6973b-124">Library</span></span><br/> | <dl> <span data-ttu-id="6973b-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6973b-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6973b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6973b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6973b-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="6973b-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




