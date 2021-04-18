---
description: Il \_ metodo RGB put specifica il colore RGB su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'IDxtKey: metodo:p ut_RGB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329631"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="cc920-104">IDxtKey: \_ metodo RGB ut:p</span><span class="sxs-lookup"><span data-stu-id="cc920-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="cc920-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="cc920-105">\[Deprecated.</span></span> <span data-ttu-id="cc920-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cc920-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cc920-107">Il `put_RGB` metodo specifica il colore RGB su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="cc920-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="cc920-108">Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="cc920-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc920-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc920-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="cc920-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc920-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc920-111">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc920-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc920-112">Specifica il colore come numero esadecimale con formato 0xRRGGBB, dove RR è il valore rosso, GG è il valore verde e BB è il valore blu.</span><span class="sxs-lookup"><span data-stu-id="cc920-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc920-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc920-113">Return value</span></span>

<span data-ttu-id="cc920-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc920-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc920-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc920-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc920-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc920-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc920-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="cc920-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc920-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc920-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cc920-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cc920-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc920-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc920-120">Requirements</span></span>



| <span data-ttu-id="cc920-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc920-121">Requirement</span></span> | <span data-ttu-id="cc920-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cc920-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc920-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc920-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cc920-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc920-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cc920-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc920-125">Library</span></span><br/> | <dl> <span data-ttu-id="cc920-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc920-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc920-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc920-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc920-128">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="cc920-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="cc920-129">**IDxtKey: tipo di:p di \_ tipo UT**</span><span class="sxs-lookup"><span data-stu-id="cc920-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




