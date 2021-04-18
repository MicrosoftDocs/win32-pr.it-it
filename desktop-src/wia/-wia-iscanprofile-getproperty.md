---
description: Ottiene il valore delle proprietà figlio specificate nell'oggetto <Properties> elemento di un profilo di analisi.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'Metodo IScanProfile:: GetProperty (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308261"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="4debd-104">Metodo IScanProfile:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="4debd-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="4debd-105">Ottiene il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="4debd-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="4debd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4debd-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="4debd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4debd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4debd-108">numero di  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4debd-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4debd-109">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="4debd-109">Type: **ULONG**</span></span>

<span data-ttu-id="4debd-110">Numero di voci nelle matrici a cui punta *PID* e *pvar*.</span><span class="sxs-lookup"><span data-stu-id="4debd-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="4debd-111">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4debd-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4debd-112">Tipo: \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="4debd-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="4debd-113">Puntatore a una matrice dei numeri di identificazione delle proprietà da impostare.</span><span class="sxs-lookup"><span data-stu-id="4debd-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="4debd-114">Ogni valore nella matrice è una [costante di proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4debd-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4debd-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4debd-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4debd-116">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="4debd-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="4debd-117">Puntatore a una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="4debd-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4debd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4debd-118">Return value</span></span>

<span data-ttu-id="4debd-119">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4debd-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4debd-120">Restituisce \_ false se uno dei valori di proprietà non è disponibile; in caso contrario, restituisce \_ un codice di errore standard com.</span><span class="sxs-lookup"><span data-stu-id="4debd-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4debd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="4debd-121">Remarks</span></span>

<span data-ttu-id="4debd-122">Il tipo di ogni valore deve essere dello stesso tipo impostato con la chiamata a [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4debd-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="4debd-123">Ogni valore nella matrice a cui punta il *PID* è una delle [costanti della proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4debd-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="4debd-124">È possibile estendere questo sistema di identificazione.</span><span class="sxs-lookup"><span data-stu-id="4debd-124">You can extend this identification system.</span></span> <span data-ttu-id="4debd-125">Vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4debd-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4debd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4debd-126">Requirements</span></span>



| <span data-ttu-id="4debd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4debd-127">Requirement</span></span> | <span data-ttu-id="4debd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4debd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4debd-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4debd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4debd-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4debd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4debd-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4debd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4debd-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4debd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4debd-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4debd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4debd-134"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4debd-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="4debd-135">IDL</span><span class="sxs-lookup"><span data-stu-id="4debd-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4debd-136"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4debd-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4debd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4debd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4debd-138">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="4debd-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="4debd-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4debd-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4debd-140">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="4debd-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="4debd-141">Costanti della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="4debd-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="4debd-142">Definizione di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="4debd-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
