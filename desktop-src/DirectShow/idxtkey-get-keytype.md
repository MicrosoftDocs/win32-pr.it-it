---
description: Il \_ metodo Get chiave Type recupera il tipo di chiave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Metodo IDxtKey:: get_KeyType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326919"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="514fb-103">Metodo IDxtKey:: Get \_ DataType</span><span class="sxs-lookup"><span data-stu-id="514fb-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="514fb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="514fb-104">\[Deprecated.</span></span> <span data-ttu-id="514fb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="514fb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="514fb-106">Il `get_KeyType` metodo recupera il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="514fb-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="514fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="514fb-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="514fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="514fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="514fb-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="514fb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="514fb-110">Riceve uno dei seguenti valori di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="514fb-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="514fb-111">Valore</span><span class="sxs-lookup"><span data-stu-id="514fb-111">Value</span></span>             | <span data-ttu-id="514fb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="514fb-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="514fb-113">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="514fb-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="514fb-114">Tasto Chroma.</span><span class="sxs-lookup"><span data-stu-id="514fb-114">Chroma key.</span></span> <span data-ttu-id="514fb-115">(Chiave su valore RGB).</span><span class="sxs-lookup"><span data-stu-id="514fb-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="514fb-116">\_NONRED DXTKEY</span><span class="sxs-lookup"><span data-stu-id="514fb-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="514fb-117">Chiave di Nonred.</span><span class="sxs-lookup"><span data-stu-id="514fb-117">Nonred key.</span></span> <span data-ttu-id="514fb-118">(Rende trasparenti le aree blu e verde).</span><span class="sxs-lookup"><span data-stu-id="514fb-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="514fb-119">\_luminanza DXTKEY</span><span class="sxs-lookup"><span data-stu-id="514fb-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="514fb-120">Chiave di luminanza.</span><span class="sxs-lookup"><span data-stu-id="514fb-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="514fb-121">DXTKEY \_ alfa</span><span class="sxs-lookup"><span data-stu-id="514fb-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="514fb-122">Chiave per valore alfa.</span><span class="sxs-lookup"><span data-stu-id="514fb-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="514fb-123">\_tonalità DXTKEY</span><span class="sxs-lookup"><span data-stu-id="514fb-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="514fb-124">Chiave per tonalità.</span><span class="sxs-lookup"><span data-stu-id="514fb-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="514fb-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="514fb-125">Return value</span></span>

<span data-ttu-id="514fb-126">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="514fb-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="514fb-127">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="514fb-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="514fb-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="514fb-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="514fb-129">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="514fb-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="514fb-130">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="514fb-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="514fb-131">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="514fb-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="514fb-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="514fb-132">Requirements</span></span>



| <span data-ttu-id="514fb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="514fb-133">Requirement</span></span> | <span data-ttu-id="514fb-134">Valore</span><span class="sxs-lookup"><span data-stu-id="514fb-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="514fb-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="514fb-135">Header</span></span><br/>  | <dl> <span data-ttu-id="514fb-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="514fb-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="514fb-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="514fb-137">Library</span></span><br/> | <dl> <span data-ttu-id="514fb-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="514fb-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514fb-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="514fb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514fb-140">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="514fb-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




