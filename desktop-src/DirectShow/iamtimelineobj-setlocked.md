---
description: Il metodo selocked imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Metodo IAMTimelineObj:: selocked (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330818"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="5ffce-103">Metodo IAMTimelineObj:: selocked</span><span class="sxs-lookup"><span data-stu-id="5ffce-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="5ffce-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5ffce-104">\[Deprecated.</span></span> <span data-ttu-id="5ffce-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ffce-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ffce-106">Il `SetLocked` metodo imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.</span><span class="sxs-lookup"><span data-stu-id="5ffce-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="5ffce-107">Uno stato bloccato indica che l'oggetto non deve essere modificato. uno stato sbloccato indica che l'oggetto può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="5ffce-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="5ffce-108">La sequenza temporale non impone il blocco.</span><span class="sxs-lookup"><span data-stu-id="5ffce-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="5ffce-109">L'impostazione bloccata esiste solo per praticità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ffce-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffce-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ffce-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="5ffce-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ffce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ffce-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="5ffce-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5ffce-113">Valore booleano che specifica lo stato di modifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ffce-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="5ffce-114">Se **true**, l'oggetto è bloccato e non deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="5ffce-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="5ffce-115">Se **false**, l'oggetto è sbloccato e può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="5ffce-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ffce-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ffce-116">Return value</span></span>

<span data-ttu-id="5ffce-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5ffce-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ffce-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ffce-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ffce-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ffce-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ffce-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5ffce-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ffce-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ffce-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5ffce-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5ffce-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ffce-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ffce-123">Requirements</span></span>



| <span data-ttu-id="5ffce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ffce-124">Requirement</span></span> | <span data-ttu-id="5ffce-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5ffce-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffce-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ffce-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5ffce-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ffce-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ffce-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ffce-128">Library</span></span><br/> | <dl> <span data-ttu-id="5ffce-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ffce-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffce-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ffce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffce-131">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="5ffce-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5ffce-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5ffce-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




