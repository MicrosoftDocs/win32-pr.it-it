---
description: Il \_ metodo Get RGB Recupera il colore RGB su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Metodo IDxtKey:: get_RGB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326916"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="bb068-104">Metodo IDxtKey:: Get \_ RGB</span><span class="sxs-lookup"><span data-stu-id="bb068-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="bb068-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bb068-105">\[Deprecated.</span></span> <span data-ttu-id="bb068-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb068-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb068-107">Il `get_RGB` metodo recupera il colore RGB su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="bb068-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="bb068-108">Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="bb068-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb068-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb068-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bb068-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb068-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb068-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bb068-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bb068-112">Riceve il colore.</span><span class="sxs-lookup"><span data-stu-id="bb068-112">Receives the color.</span></span> <span data-ttu-id="bb068-113">Il valore restituito è un numero esadecimale con formato 0xRRGGBB, dove RR è il valore rosso, GG è il valore verde e BB è il valore blu.</span><span class="sxs-lookup"><span data-stu-id="bb068-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb068-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb068-114">Return value</span></span>

<span data-ttu-id="bb068-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb068-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb068-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb068-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb068-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb068-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bb068-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bb068-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb068-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb068-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bb068-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bb068-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb068-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb068-121">Requirements</span></span>



| <span data-ttu-id="bb068-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb068-122">Requirement</span></span> | <span data-ttu-id="bb068-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bb068-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb068-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb068-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bb068-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb068-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb068-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb068-126">Library</span></span><br/> | <dl> <span data-ttu-id="bb068-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb068-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb068-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb068-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb068-129">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="bb068-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="bb068-130">**Tipo di IDxtKey:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="bb068-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




