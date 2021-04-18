---
description: Il Metodo GetUserId recupera l'identificatore definito dall'applicazione dell'oggetto.
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: 'Metodo IAMTimelineObj:: GetUserID (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f5d6c07fd826f2045ddc9f54445bc96feb5a7c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324001"
---
# <a name="iamtimelineobjgetuserid-method"></a><span data-ttu-id="054d9-103">Metodo IAMTimelineObj:: GetUserID</span><span class="sxs-lookup"><span data-stu-id="054d9-103">IAMTimelineObj::GetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="054d9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="054d9-104">\[Deprecated.</span></span> <span data-ttu-id="054d9-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="054d9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="054d9-106">Il `GetUserID` metodo recupera l'identificatore definito dall'applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="054d9-106">The `GetUserID` method retrieves the object's application-defined identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="054d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="054d9-107">Syntax</span></span>


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="054d9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="054d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="054d9-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="054d9-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="054d9-110">Riceve l'identificatore definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="054d9-110">Receives the application-defined identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="054d9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="054d9-111">Return value</span></span>

<span data-ttu-id="054d9-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="054d9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="054d9-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="054d9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="054d9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="054d9-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="054d9-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="054d9-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="054d9-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="054d9-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="054d9-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="054d9-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="054d9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="054d9-118">Requirements</span></span>



| <span data-ttu-id="054d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="054d9-119">Requirement</span></span> | <span data-ttu-id="054d9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="054d9-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="054d9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="054d9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="054d9-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="054d9-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="054d9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="054d9-123">Library</span></span><br/> | <dl> <span data-ttu-id="054d9-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="054d9-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="054d9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="054d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="054d9-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="054d9-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="054d9-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="054d9-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




