---
description: Imposta il valore delle proprietà figlio specificate nell'oggetto <Properties> elemento di un profilo di analisi.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Metodo IScanProfile:: SetProperty (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752855"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="dc6b0-104">Metodo IScanProfile:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="dc6b0-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="dc6b0-105">Imposta il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6b0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc6b0-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="dc6b0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc6b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc6b0-108">numero di  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc6b0-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc6b0-109">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="dc6b0-109">Type: **ULONG**</span></span>

<span data-ttu-id="dc6b0-110">Numero di voci nelle matrici a cui punta *PID* e *pvar*.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="dc6b0-111">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc6b0-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc6b0-112">Tipo: \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="dc6b0-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="dc6b0-113">Puntatore a una matrice di numeri di identificazione delle proprietà da impostare.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="dc6b0-114">Ogni valore nella matrice è una [costante di proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dc6b0-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc6b0-115">_pvar \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc6b0-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc6b0-116">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="dc6b0-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="dc6b0-117">Puntatore a una matrice di valori da assegnare alle proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc6b0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc6b0-118">Return value</span></span>

<span data-ttu-id="dc6b0-119">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dc6b0-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dc6b0-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc6b0-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc6b0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc6b0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc6b0-122">Remarks</span></span>

<span data-ttu-id="dc6b0-123">Ogni valore nella matrice a cui punta il *PID* è una delle [costanti della proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dc6b0-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="dc6b0-124">È possibile estendere questo sistema di identificazione.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-124">You can extend this identification system.</span></span> <span data-ttu-id="dc6b0-125">Vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dc6b0-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="dc6b0-126">Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="dc6b0-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="dc6b0-127">Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc6b0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc6b0-128">Requirements</span></span>



| <span data-ttu-id="dc6b0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc6b0-129">Requirement</span></span> | <span data-ttu-id="dc6b0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6b0-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6b0-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc6b0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6b0-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc6b0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="dc6b0-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc6b0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6b0-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc6b0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc6b0-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc6b0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc6b0-136"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc6b0-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="dc6b0-137">IDL</span><span class="sxs-lookup"><span data-stu-id="dc6b0-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc6b0-138"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc6b0-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc6b0-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc6b0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc6b0-140">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="dc6b0-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="dc6b0-141">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="dc6b0-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6b0-142">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="dc6b0-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="dc6b0-143">Costanti della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="dc6b0-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="dc6b0-144">Definizione di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="dc6b0-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
