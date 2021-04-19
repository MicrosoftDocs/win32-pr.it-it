---
description: Il \_ metodo Get Size restituisce le dimensioni di output e la modalità di estensione correnti.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Metodo IResize:: get_Size (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332568"
---
# <a name="iresizeget_size-method"></a><span data-ttu-id="7ab38-103">Metodo IResize:: Get \_ size</span><span class="sxs-lookup"><span data-stu-id="7ab38-103">IResize::get\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="7ab38-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7ab38-104">\[Deprecated.</span></span> <span data-ttu-id="7ab38-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ab38-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ab38-106">Il `get_Size` metodo restituisce le dimensioni di output e la modalità di estensione correnti.</span><span class="sxs-lookup"><span data-stu-id="7ab38-106">The `get_Size` method returns the current output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab38-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ab38-107">Syntax</span></span>


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a><span data-ttu-id="7ab38-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ab38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab38-109">*piHeight* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ab38-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab38-110">Riceve l'altezza del video in pixel.</span><span class="sxs-lookup"><span data-stu-id="7ab38-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7ab38-111">*piWidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ab38-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab38-112">Riceve la larghezza del video in pixel.</span><span class="sxs-lookup"><span data-stu-id="7ab38-112">Receives the video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7ab38-113">*PFLAG* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ab38-113">*pFlag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab38-114">Riceve un flag che specifica la modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="7ab38-114">Receives a flag specifying the stretch mode.</span></span> <span data-ttu-id="7ab38-115">Per i valori possibili, vedere [**ridimensionare i flag**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="7ab38-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab38-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ab38-116">Return value</span></span>

<span data-ttu-id="7ab38-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ab38-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ab38-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ab38-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ab38-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ab38-119">Remarks</span></span>

<span data-ttu-id="7ab38-120">Se il tipo di output non è stato impostato, il filtro deve restituire valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="7ab38-120">If the output type has not been set, the filter should return default values.</span></span> <span data-ttu-id="7ab38-121">Questi valori possono essere scelti arbitrariamente in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="7ab38-121">These values can be arbitrarily chosen at design time.</span></span>

> [!Note]  
> <span data-ttu-id="7ab38-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7ab38-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ab38-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ab38-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ab38-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7ab38-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ab38-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ab38-125">Requirements</span></span>



| <span data-ttu-id="7ab38-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab38-126">Requirement</span></span> | <span data-ttu-id="7ab38-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7ab38-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab38-128">Versione</span><span class="sxs-lookup"><span data-stu-id="7ab38-128">Version</span></span><br/> | <span data-ttu-id="7ab38-129">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7ab38-129">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="7ab38-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ab38-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7ab38-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab38-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ab38-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ab38-132">Library</span></span><br/> | <dl> <span data-ttu-id="7ab38-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ab38-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab38-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ab38-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab38-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7ab38-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="7ab38-136">**Interfaccia IResize**</span><span class="sxs-lookup"><span data-stu-id="7ab38-136">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




