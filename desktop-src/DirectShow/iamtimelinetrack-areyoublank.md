---
description: Il metodo AreYouBlank determina se la traccia è vuota (non contiene oggetti di origine).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'Metodo IAMTimelineTrack:: AreYouBlank (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325175"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="b2a01-103">Metodo IAMTimelineTrack:: AreYouBlank</span><span class="sxs-lookup"><span data-stu-id="b2a01-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="b2a01-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b2a01-104">\[Deprecated.</span></span> <span data-ttu-id="b2a01-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2a01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2a01-106">Il `AreYouBlank` metodo determina se la traccia è vuota (non contiene oggetti di origine).</span><span class="sxs-lookup"><span data-stu-id="b2a01-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a01-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2a01-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b2a01-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2a01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a01-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="b2a01-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b2a01-110">Riceve un valore booleano che specifica se la traccia è vuota.</span><span class="sxs-lookup"><span data-stu-id="b2a01-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="b2a01-111">Se il valore è **true**, la traccia è vuota e non contiene oggetti di origine.</span><span class="sxs-lookup"><span data-stu-id="b2a01-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="b2a01-112">Se **false**, la traccia non è vuota.</span><span class="sxs-lookup"><span data-stu-id="b2a01-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a01-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2a01-113">Return value</span></span>

<span data-ttu-id="b2a01-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2a01-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2a01-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2a01-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a01-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2a01-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b2a01-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b2a01-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2a01-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2a01-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2a01-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b2a01-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2a01-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2a01-120">Requirements</span></span>



| <span data-ttu-id="b2a01-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2a01-121">Requirement</span></span> | <span data-ttu-id="b2a01-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b2a01-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a01-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2a01-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b2a01-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2a01-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2a01-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2a01-125">Library</span></span><br/> | <dl> <span data-ttu-id="b2a01-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2a01-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2a01-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2a01-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a01-128">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="b2a01-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="b2a01-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b2a01-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




