---
description: 'Il metodo GetMediaLength2 recupera la lunghezza del supporto di questo oggetto di origine. Questo metodo è equivalente a IAMTimelineSrc:: GetMediaLength, ma accetta valori REFTIME.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Metodo IAMTimelineSrc:: GetMediaLength2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324260"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="5fbd8-104">Metodo IAMTimelineSrc:: GetMediaLength2</span><span class="sxs-lookup"><span data-stu-id="5fbd8-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="5fbd8-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-105">\[Deprecated.</span></span> <span data-ttu-id="5fbd8-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5fbd8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5fbd8-107">Il `GetMediaLength2` metodo recupera la lunghezza del supporto di questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="5fbd8-108">Questo metodo è equivalente a [**IAMTimelineSrc:: GetMediaLength**](iamtimelinesrc-getmedialength.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="5fbd8-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbd8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fbd8-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="5fbd8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fbd8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fbd8-111">*pLength*</span><span class="sxs-lookup"><span data-stu-id="5fbd8-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="5fbd8-112">Riceve la lunghezza del supporto in secondi.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fbd8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fbd8-113">Return value</span></span>

<span data-ttu-id="5fbd8-114">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="5fbd8-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="5fbd8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5fbd8-115">Return code</span></span>                                                                                     | <span data-ttu-id="5fbd8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fbd8-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="5fbd8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="5fbd8-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="5fbd8-119"><dt>**E \_ NOTDETERMINED**</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="5fbd8-120">I tempi dei supporti non sono impostati per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="5fbd8-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="5fbd8-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="5fbd8-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="5fbd8-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fbd8-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5fbd8-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5fbd8-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5fbd8-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5fbd8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fbd8-127">Requirements</span></span>



| <span data-ttu-id="5fbd8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fbd8-128">Requirement</span></span> | <span data-ttu-id="5fbd8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5fbd8-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbd8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fbd8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5fbd8-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5fbd8-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fbd8-132">Library</span></span><br/> | <dl> <span data-ttu-id="5fbd8-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbd8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fbd8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbd8-135">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="5fbd8-136">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5fbd8-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




