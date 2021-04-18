---
description: Il metodo getlocked recupera lo stato di modifica dell'oggetto (bloccato o sbloccato).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Metodo IAMTimelineObj:: getlocked (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331274"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="e32c8-103">Metodo IAMTimelineObj:: getlocked</span><span class="sxs-lookup"><span data-stu-id="e32c8-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="e32c8-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e32c8-104">\[Deprecated.</span></span> <span data-ttu-id="e32c8-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e32c8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e32c8-106">Il `GetLocked` metodo recupera lo stato di modifica dell'oggetto (bloccato o sbloccato).</span><span class="sxs-lookup"><span data-stu-id="e32c8-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="e32c8-107">Uno stato bloccato indica che l'oggetto non deve essere modificato. uno stato sbloccato indica che l'oggetto può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="e32c8-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="e32c8-108">La sequenza temporale non impone il blocco.</span><span class="sxs-lookup"><span data-stu-id="e32c8-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="e32c8-109">L'impostazione bloccata esiste solo per praticità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e32c8-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32c8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e32c8-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e32c8-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e32c8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32c8-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e32c8-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e32c8-113">Riceve lo stato di modifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e32c8-113">Receives the object's editing state.</span></span> <span data-ttu-id="e32c8-114">Se il valore è **true**, l'oggetto è bloccato e non deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="e32c8-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="e32c8-115">Se **false**, l'oggetto è sbloccato e può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="e32c8-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e32c8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e32c8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e32c8-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e32c8-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e32c8-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e32c8-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e32c8-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e32c8-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e32c8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e32c8-120">Requirements</span></span>



| <span data-ttu-id="e32c8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e32c8-121">Requirement</span></span> | <span data-ttu-id="e32c8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e32c8-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e32c8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e32c8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e32c8-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e32c8-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e32c8-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e32c8-125">Library</span></span><br/> | <dl> <span data-ttu-id="e32c8-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e32c8-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e32c8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e32c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32c8-128">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e32c8-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e32c8-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e32c8-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




