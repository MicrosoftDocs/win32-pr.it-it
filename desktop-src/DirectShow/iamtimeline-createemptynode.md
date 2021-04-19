---
description: Il metodo CreateEmptyNode crea un nuovo oggetto sequenza temporale.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Metodo IAMTimeline:: CreateEmptyNode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326802"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="7c5b1-103">Metodo IAMTimeline:: CreateEmptyNode</span><span class="sxs-lookup"><span data-stu-id="7c5b1-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="7c5b1-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-104">\[Deprecated.</span></span> <span data-ttu-id="7c5b1-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c5b1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7c5b1-106">Il `CreateEmptyNode` metodo crea un nuovo oggetto sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="7c5b1-107">Utilizzare questo metodo per creare oggetti sequenza temporale anziché la funzione **CoCreateInstance** , perché questo metodo esegue routine di inizializzazione importanti.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="7c5b1-108">Ogni oggetto creato da questo metodo supporta almeno l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) , insieme ad altre interfacce specifiche per quel tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5b1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c5b1-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="7c5b1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c5b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c5b1-111">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7c5b1-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c5b1-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7c5b1-113">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="7c5b1-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="7c5b1-114">Membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che specifica il tipo di oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c5b1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c5b1-115">Return value</span></span>

<span data-ttu-id="7c5b1-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7c5b1-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c5b1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c5b1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c5b1-118">Remarks</span></span>

<span data-ttu-id="7c5b1-119">Non aggiungere il nuovo oggetto a un'altra istanza della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="7c5b1-120">Ogni oggetto in una sequenza temporale deve essere creato da tale sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="7c5b1-121">Se il metodo ha esito positivo, l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="7c5b1-122">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="7c5b1-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7c5b1-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c5b1-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7c5b1-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7c5b1-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c5b1-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c5b1-126">Requirements</span></span>



| <span data-ttu-id="7c5b1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c5b1-127">Requirement</span></span> | <span data-ttu-id="7c5b1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7c5b1-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5b1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c5b1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7c5b1-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c5b1-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7c5b1-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c5b1-131">Library</span></span><br/> | <dl> <span data-ttu-id="7c5b1-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c5b1-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c5b1-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c5b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5b1-134">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="7c5b1-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="7c5b1-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7c5b1-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




