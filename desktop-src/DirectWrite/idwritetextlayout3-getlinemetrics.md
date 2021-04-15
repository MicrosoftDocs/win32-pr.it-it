---
title: Metodo IDWriteTextLayout3 GetLineMetrics
description: Recupera le proprietà di ogni riga.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Scrittura diretta metodo GetLineMetrics
- Metodo GetLineMetrics scrittura diretta, interfaccia IDWriteTextLayout3
- IDWriteTextLayout3 Interface Direct Write, metodo GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477518"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="cf875-106">Metodo IDWriteTextLayout3:: GetLineMetrics</span><span class="sxs-lookup"><span data-stu-id="cf875-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="cf875-107">Recupera le proprietà di ogni riga.</span><span class="sxs-lookup"><span data-stu-id="cf875-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf875-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf875-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="cf875-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf875-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf875-110">*lineMetrics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf875-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf875-111">Matrice da riempire con le informazioni sulla riga.</span><span class="sxs-lookup"><span data-stu-id="cf875-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="cf875-112">*maxLineCount*</span><span class="sxs-lookup"><span data-stu-id="cf875-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="cf875-113">Dimensione massima della matrice lineMetrics.</span><span class="sxs-lookup"><span data-stu-id="cf875-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="cf875-114">*actualLineCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf875-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf875-115">Dimensioni effettive della matrice lineMetrics necessaria.</span><span class="sxs-lookup"><span data-stu-id="cf875-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf875-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf875-116">Return value</span></span>

<span data-ttu-id="cf875-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cf875-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf875-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf875-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf875-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf875-119">Remarks</span></span>

<span data-ttu-id="cf875-120">Se maxLineCount non è sufficientemente grande E \_ non è \_ sufficiente \_ un buffer, equivalente a HRESULT \_ di \_ Win32 (errore \_ buffer insufficiente \_ ), viene restituito e actualLineCount è impostato sul numero di righe necessarie.</span><span class="sxs-lookup"><span data-stu-id="cf875-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf875-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf875-121">Requirements</span></span>



| <span data-ttu-id="cf875-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf875-122">Requirement</span></span> | <span data-ttu-id="cf875-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cf875-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf875-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf875-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf875-125">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf875-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cf875-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf875-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf875-127">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf875-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf875-128">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf875-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="cf875-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="cf875-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="cf875-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf875-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf875-131"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf875-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cf875-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cf875-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf875-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf875-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf875-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf875-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf875-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="cf875-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





