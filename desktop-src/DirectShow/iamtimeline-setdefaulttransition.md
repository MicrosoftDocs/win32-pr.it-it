---
description: Il metodo SetDefaultTransition imposta la transizione predefinita. Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'Metodo IAMTimeline:: SetDefaultTransition (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332766"
---
# <a name="iamtimelinesetdefaulttransition-method"></a><span data-ttu-id="79f99-104">Metodo IAMTimeline:: SetDefaultTransition</span><span class="sxs-lookup"><span data-stu-id="79f99-104">IAMTimeline::SetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="79f99-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="79f99-105">\[Deprecated.</span></span> <span data-ttu-id="79f99-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="79f99-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="79f99-107">Il `SetDefaultTransition` metodo imposta la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="79f99-107">The `SetDefaultTransition` method sets the default transition.</span></span> <span data-ttu-id="79f99-108">Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="79f99-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f99-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79f99-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="79f99-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="79f99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f99-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="79f99-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="79f99-112">Puntatore a una variabile che contiene il GUID della transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="79f99-112">Pointer to a variable that contains the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f99-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79f99-113">Return value</span></span>

<span data-ttu-id="79f99-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="79f99-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79f99-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79f99-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="79f99-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="79f99-116">Remarks</span></span>

<span data-ttu-id="79f99-117">Se non si imposta una transizione predefinita o se la transizione specificata come impostazione predefinita genera un errore, DES utilizza una propria transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="79f99-117">If you do not set a default transition, or if the transition that you specify as a default causes an error, DES uses its own default transition.</span></span>

> [!Note]  
> <span data-ttu-id="79f99-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="79f99-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="79f99-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="79f99-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="79f99-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="79f99-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79f99-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79f99-121">Requirements</span></span>



| <span data-ttu-id="79f99-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79f99-122">Requirement</span></span> | <span data-ttu-id="79f99-123">Valore</span><span class="sxs-lookup"><span data-stu-id="79f99-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79f99-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79f99-124">Header</span></span><br/>  | <dl> <span data-ttu-id="79f99-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f99-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="79f99-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="79f99-126">Library</span></span><br/> | <dl> <span data-ttu-id="79f99-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79f99-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f99-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79f99-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f99-129">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="79f99-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="79f99-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="79f99-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




