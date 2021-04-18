---
description: Il metodo seuserid imposta un identificatore definito dall'applicazione per l'oggetto.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'Metodo IAMTimelineObj:: seuserid (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330800"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="7e834-103">Metodo IAMTimelineObj:: seuserid</span><span class="sxs-lookup"><span data-stu-id="7e834-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="7e834-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7e834-104">\[Deprecated.</span></span> <span data-ttu-id="7e834-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7e834-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7e834-106">Il `SetUserID` metodo imposta un identificatore definito dall'applicazione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7e834-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e834-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e834-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="7e834-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e834-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e834-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="7e834-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="7e834-110">Valore che specifica l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="7e834-110">Value that specifies the identifier.</span></span> <span data-ttu-id="7e834-111">Questo identificatore viene usato solo dall'applicazione e può essere qualsiasi valore.</span><span class="sxs-lookup"><span data-stu-id="7e834-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e834-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e834-112">Return value</span></span>

<span data-ttu-id="7e834-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7e834-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7e834-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e834-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e834-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e834-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7e834-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7e834-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7e834-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7e834-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7e834-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7e834-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e834-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e834-119">Requirements</span></span>



| <span data-ttu-id="7e834-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e834-120">Requirement</span></span> | <span data-ttu-id="7e834-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7e834-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e834-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e834-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7e834-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e834-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7e834-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="7e834-124">Library</span></span><br/> | <dl> <span data-ttu-id="7e834-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e834-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e834-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e834-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e834-127">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="7e834-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="7e834-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7e834-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




