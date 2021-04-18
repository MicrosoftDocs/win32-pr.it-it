---
description: Il metodo getgenid recupera l'identificatore generato dall'oggetto. L'identificatore è un numero riservato; le applicazioni non devono utilizzarlo.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Metodo IAMTimelineObj:: getgenid (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331279"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="e3a26-104">Metodo IAMTimelineObj:: getgenid</span><span class="sxs-lookup"><span data-stu-id="e3a26-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="e3a26-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e3a26-105">\[Deprecated.</span></span> <span data-ttu-id="e3a26-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3a26-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e3a26-107">Il `GetGenID` metodo recupera l'identificatore generato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e3a26-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="e3a26-108">L'identificatore è un numero riservato; le applicazioni non devono utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="e3a26-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a26-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3a26-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e3a26-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3a26-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a26-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e3a26-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a26-112">Riceve l'identificatore generato.</span><span class="sxs-lookup"><span data-stu-id="e3a26-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a26-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3a26-113">Return value</span></span>

<span data-ttu-id="e3a26-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3a26-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3a26-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3a26-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a26-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a26-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3a26-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e3a26-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3a26-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3a26-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e3a26-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e3a26-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3a26-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a26-120">Requirements</span></span>



| <span data-ttu-id="e3a26-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a26-121">Requirement</span></span> | <span data-ttu-id="e3a26-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a26-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a26-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3a26-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a26-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a26-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e3a26-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3a26-125">Library</span></span><br/> | <dl> <span data-ttu-id="e3a26-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3a26-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a26-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a26-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e3a26-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e3a26-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e3a26-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




