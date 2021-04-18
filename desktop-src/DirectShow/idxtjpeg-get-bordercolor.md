---
description: Il \_ metodo Get BorderColor Recupera il colore del bordo intorno ai bordi del pattern di cancellazione.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'Metodo IDxtJpeg:: get_BorderColor (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331509"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="10c6d-103">Metodo IDxtJpeg:: Get \_ BorderColor</span><span class="sxs-lookup"><span data-stu-id="10c6d-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="10c6d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="10c6d-104">\[Deprecated.</span></span> <span data-ttu-id="10c6d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10c6d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="10c6d-106">Il `get_BorderColor` metodo recupera il colore del bordo intorno ai bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="10c6d-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c6d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10c6d-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="10c6d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10c6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c6d-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="10c6d-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="10c6d-110">Riceve il colore.</span><span class="sxs-lookup"><span data-stu-id="10c6d-110">Receives the color.</span></span> <span data-ttu-id="10c6d-111">Il valore restituito è un numero esadecimale con formato 0xRRGGBB, dove RR è il valore rosso, GG è il valore verde e BB è il valore blu.</span><span class="sxs-lookup"><span data-stu-id="10c6d-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c6d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10c6d-112">Return value</span></span>

<span data-ttu-id="10c6d-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="10c6d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="10c6d-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10c6d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c6d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="10c6d-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="10c6d-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="10c6d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="10c6d-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="10c6d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="10c6d-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="10c6d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10c6d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10c6d-119">Requirements</span></span>



| <span data-ttu-id="10c6d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c6d-120">Requirement</span></span> | <span data-ttu-id="10c6d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="10c6d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10c6d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10c6d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="10c6d-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c6d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="10c6d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="10c6d-124">Library</span></span><br/> | <dl> <span data-ttu-id="10c6d-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10c6d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c6d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10c6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c6d-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="10c6d-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




