---
description: Il \_ metodo Put Alpha specifica il valore alfa per l'intera immagine.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter: metodo:p ut_Alpha (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329755"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="8ac93-103">IDxtAlphaSetter: metodo:p UT \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="8ac93-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="8ac93-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8ac93-104">\[Deprecated.</span></span> <span data-ttu-id="8ac93-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ac93-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ac93-106">Il `put_Alpha` metodo specifica il valore alfa per l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="8ac93-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac93-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ac93-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="8ac93-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ac93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac93-109">*Alfa* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ac93-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac93-110">Valore alfa.</span><span class="sxs-lookup"><span data-stu-id="8ac93-110">The alpha value.</span></span> <span data-ttu-id="8ac93-111">Questo valore verrà applicato all'intera immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ac93-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="8ac93-112">Per disabilitare questa proprietà, impostare un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="8ac93-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac93-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ac93-113">Return value</span></span>

<span data-ttu-id="8ac93-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ac93-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ac93-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ac93-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac93-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ac93-116">Remarks</span></span>

<span data-ttu-id="8ac93-117">Se si imposta questa proprietà su un valore non negativo, è necessario disabilitare anche la proprietà Alpha ramp, chiamando **put \_ AlphaRamp** con un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="8ac93-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="8ac93-118">In caso contrario, non viene eseguito il rendering corretto dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="8ac93-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="8ac93-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8ac93-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ac93-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ac93-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ac93-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8ac93-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ac93-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ac93-122">Requirements</span></span>



| <span data-ttu-id="8ac93-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac93-123">Requirement</span></span> | <span data-ttu-id="8ac93-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8ac93-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac93-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ac93-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8ac93-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac93-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ac93-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ac93-127">Library</span></span><br/> | <dl> <span data-ttu-id="8ac93-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ac93-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac93-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ac93-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac93-130">**Interfaccia IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="8ac93-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="8ac93-131">**IDxtAlphaSetter::p UT \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="8ac93-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




