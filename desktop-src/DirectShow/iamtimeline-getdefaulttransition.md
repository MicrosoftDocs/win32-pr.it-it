---
description: Il metodo GetDefaultTransition recupera la transizione predefinita. Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Metodo IAMTimeline:: GetDefaultTransition (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331097"
---
# <a name="iamtimelinegetdefaulttransition-method"></a><span data-ttu-id="47367-104">Metodo IAMTimeline:: GetDefaultTransition</span><span class="sxs-lookup"><span data-stu-id="47367-104">IAMTimeline::GetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="47367-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="47367-105">\[Deprecated.</span></span> <span data-ttu-id="47367-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47367-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="47367-107">Il `GetDefaultTransition` metodo recupera la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="47367-107">The `GetDefaultTransition` method retrieves the default transition.</span></span> <span data-ttu-id="47367-108">Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="47367-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="47367-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47367-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="47367-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="47367-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47367-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="47367-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="47367-112">Riceve il GUID della transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="47367-112">Receives the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47367-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47367-113">Return value</span></span>

<span data-ttu-id="47367-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="47367-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="47367-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="47367-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="47367-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="47367-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="47367-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="47367-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="47367-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="47367-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="47367-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="47367-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47367-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47367-120">Requirements</span></span>



| <span data-ttu-id="47367-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="47367-121">Requirement</span></span> | <span data-ttu-id="47367-122">Valore</span><span class="sxs-lookup"><span data-stu-id="47367-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47367-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47367-123">Header</span></span><br/>  | <dl> <span data-ttu-id="47367-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="47367-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="47367-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="47367-125">Library</span></span><br/> | <dl> <span data-ttu-id="47367-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47367-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47367-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47367-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47367-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="47367-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="47367-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="47367-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




