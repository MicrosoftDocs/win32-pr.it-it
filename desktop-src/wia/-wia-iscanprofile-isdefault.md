---
description: Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo IWiaItem2 associato.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Metodo IScanProfile:: IsDefault (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966841"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="93c1f-103">Metodo IScanProfile:: IsDefault</span><span class="sxs-lookup"><span data-stu-id="93c1f-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="93c1f-104">Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associato.</span><span class="sxs-lookup"><span data-stu-id="93c1f-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93c1f-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="93c1f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c1f-107">*pbDefault* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93c1f-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c1f-108">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="93c1f-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="93c1f-109">Puntatore a _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="93c1f-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="93c1f-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span><span class="sxs-lookup"><span data-stu-id="93c1f-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="93c1f-111">Il profilo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="93c1f-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="93c1f-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span><span class="sxs-lookup"><span data-stu-id="93c1f-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="93c1f-113">Il profilo non è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="93c1f-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c1f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93c1f-114">Return value</span></span>

<span data-ttu-id="93c1f-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="93c1f-115">Type: **HRESULT**</span></span>

<span data-ttu-id="93c1f-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="93c1f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93c1f-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93c1f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c1f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="93c1f-118">Remarks</span></span>

<span data-ttu-id="93c1f-119">*pbDefault* è **true** se il profilo contiene un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="93c1f-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="93c1f-120">È **false** se tale elemento non è presente.</span><span class="sxs-lookup"><span data-stu-id="93c1f-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="93c1f-121">L'elemento non ha alcun valore.</span><span class="sxs-lookup"><span data-stu-id="93c1f-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c1f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93c1f-122">Requirements</span></span>



| <span data-ttu-id="93c1f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c1f-123">Requirement</span></span> | <span data-ttu-id="93c1f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="93c1f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c1f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c1f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93c1f-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93c1f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="93c1f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c1f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93c1f-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93c1f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93c1f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93c1f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c1f-130"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c1f-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="93c1f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="93c1f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93c1f-132"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93c1f-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c1f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93c1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c1f-134">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="93c1f-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="93c1f-135">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="93c1f-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




