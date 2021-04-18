---
description: Il \_ metodo Put chiave Type specifica il tipo di chiave.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: 'IDxtKey: metodo:p ut_KeyType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326904"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="ec179-103">IDxtKey::p \_ metodo di tipo UT</span><span class="sxs-lookup"><span data-stu-id="ec179-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="ec179-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ec179-104">\[Deprecated.</span></span> <span data-ttu-id="ec179-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec179-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ec179-106">Il `put_KeyType` metodo specifica il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="ec179-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec179-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec179-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="ec179-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec179-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec179-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec179-110">Specifica il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="ec179-110">Specifies the key type.</span></span> <span data-ttu-id="ec179-111">Questo parametro deve essere uno dei seguenti valori di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ec179-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="ec179-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ec179-112">Value</span></span>             | <span data-ttu-id="ec179-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec179-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ec179-114">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="ec179-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="ec179-115">Tasto Chroma.</span><span class="sxs-lookup"><span data-stu-id="ec179-115">Chroma key.</span></span> <span data-ttu-id="ec179-116">(Chiave su valore RGB).</span><span class="sxs-lookup"><span data-stu-id="ec179-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="ec179-117">\_NONRED DXTKEY</span><span class="sxs-lookup"><span data-stu-id="ec179-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="ec179-118">Chiave di Nonred.</span><span class="sxs-lookup"><span data-stu-id="ec179-118">Nonred key.</span></span> <span data-ttu-id="ec179-119">(Rende trasparenti le aree blu e verde).</span><span class="sxs-lookup"><span data-stu-id="ec179-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="ec179-120">\_luminanza DXTKEY</span><span class="sxs-lookup"><span data-stu-id="ec179-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="ec179-121">Chiave di luminanza.</span><span class="sxs-lookup"><span data-stu-id="ec179-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="ec179-122">DXTKEY \_ alfa</span><span class="sxs-lookup"><span data-stu-id="ec179-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="ec179-123">Chiave per valore alfa.</span><span class="sxs-lookup"><span data-stu-id="ec179-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="ec179-124">\_tonalità DXTKEY</span><span class="sxs-lookup"><span data-stu-id="ec179-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="ec179-125">Chiave per tonalità.</span><span class="sxs-lookup"><span data-stu-id="ec179-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec179-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec179-126">Return value</span></span>

<span data-ttu-id="ec179-127">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ec179-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec179-128">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec179-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec179-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec179-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ec179-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ec179-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec179-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec179-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ec179-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ec179-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec179-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec179-133">Requirements</span></span>



| <span data-ttu-id="ec179-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec179-134">Requirement</span></span> | <span data-ttu-id="ec179-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ec179-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec179-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec179-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ec179-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec179-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec179-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec179-138">Library</span></span><br/> | <dl> <span data-ttu-id="ec179-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec179-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec179-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec179-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec179-141">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="ec179-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




