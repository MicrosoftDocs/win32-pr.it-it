---
description: Il \_ Metodo luminanza put specifica il valore della luminanza su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ luminanza.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'IDxtKey: metodo:p ut_Luminance (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330399"
---
# <a name="idxtkeyput_luminance-method"></a><span data-ttu-id="0f460-104">IDxtKey::p \_ metodo di luminanza UT</span><span class="sxs-lookup"><span data-stu-id="0f460-104">IDxtKey::put\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="0f460-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0f460-105">\[Deprecated.</span></span> <span data-ttu-id="0f460-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f460-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f460-107">Il `put_Luminance` metodo specifica il valore della luminanza su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="0f460-107">The `put_Luminance` method specifies the luminance value on which to key.</span></span> <span data-ttu-id="0f460-108">Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ luminanza.</span><span class="sxs-lookup"><span data-stu-id="0f460-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f460-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f460-109">Syntax</span></span>


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="0f460-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f460-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f460-111">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f460-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f460-112">Valore di luminanza su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="0f460-112">The luminance value on which to key.</span></span> <span data-ttu-id="0f460-113">L'intervallo valido è compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="0f460-113">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f460-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f460-114">Return value</span></span>

<span data-ttu-id="0f460-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f460-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f460-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f460-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f460-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f460-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f460-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0f460-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0f460-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f460-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0f460-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0f460-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f460-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f460-121">Requirements</span></span>



| <span data-ttu-id="0f460-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f460-122">Requirement</span></span> | <span data-ttu-id="0f460-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0f460-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f460-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f460-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0f460-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f460-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0f460-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="0f460-126">Library</span></span><br/> | <dl> <span data-ttu-id="0f460-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f460-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f460-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f460-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f460-129">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="0f460-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="0f460-130">**IDxtKey: tipo di:p di \_ tipo UT**</span><span class="sxs-lookup"><span data-stu-id="0f460-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




