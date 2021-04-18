---
description: Il metodo GetSubObjectGUID Recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale.
ms.assetid: c2787e6b-ed72-4a6c-9e1e-c79c00020585
title: 'Metodo IAMTimelineObj:: GetSubObjectGUID (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1c787bdbca8bbd255ccc78c3756fd0071d22f30d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328153"
---
# <a name="iamtimelineobjgetsubobjectguid-method"></a><span data-ttu-id="e9782-103">Metodo IAMTimelineObj:: GetSubObjectGUID</span><span class="sxs-lookup"><span data-stu-id="e9782-103">IAMTimelineObj::GetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="e9782-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e9782-104">\[Deprecated.</span></span> <span data-ttu-id="e9782-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9782-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e9782-106">Il `GetSubObjectGUID` metodo recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="e9782-106">The `GetSubObjectGUID` method retrieves the GUID of the subobject associated with this timeline object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9782-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9782-107">Syntax</span></span>


```C++
HRESULT GetSubObjectGUID(
   GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e9782-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9782-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9782-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e9782-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e9782-110">Riceve il GUID dell'oggetto SubObject oppure il GUID \_ null se l'oggetto non dispone di un oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="e9782-110">Receives the GUID of the subobject, or GUID\_NULL if the object does not have a subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9782-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9782-111">Return value</span></span>

<span data-ttu-id="e9782-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e9782-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9782-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9782-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9782-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9782-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9782-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e9782-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9782-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9782-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e9782-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e9782-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9782-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9782-118">Requirements</span></span>



| <span data-ttu-id="e9782-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9782-119">Requirement</span></span> | <span data-ttu-id="e9782-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e9782-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9782-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9782-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e9782-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9782-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e9782-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9782-123">Library</span></span><br/> | <dl> <span data-ttu-id="e9782-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9782-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9782-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9782-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9782-126">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e9782-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e9782-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e9782-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




