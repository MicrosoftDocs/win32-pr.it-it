---
description: Rimuove un elenco specificato di proprietà figlio nell'oggetto <Properties> elemento di un profilo di analisi.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Metodo IScanProfile:: RemoveProperty (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130026"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="84a1a-104">Metodo IScanProfile:: RemoveProperty</span><span class="sxs-lookup"><span data-stu-id="84a1a-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="84a1a-105">Rimuove un elenco specificato di proprietà figlio nell' `<Properties>` elemento di un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="84a1a-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a1a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84a1a-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="84a1a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="84a1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a1a-108">numero di  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84a1a-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84a1a-109">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="84a1a-109">Type: **ULONG**</span></span>

<span data-ttu-id="84a1a-110">Numero di voci nella matrice a cui punta il *PID* .</span><span class="sxs-lookup"><span data-stu-id="84a1a-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="84a1a-111">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84a1a-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84a1a-112">Tipo: \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="84a1a-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="84a1a-113">Puntatore a una matrice di numeri di identificazione delle proprietà da eliminare.</span><span class="sxs-lookup"><span data-stu-id="84a1a-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="84a1a-114">Ogni è una [costante di proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="84a1a-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a1a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84a1a-115">Return value</span></span>

<span data-ttu-id="84a1a-116">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="84a1a-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="84a1a-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="84a1a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84a1a-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="84a1a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="84a1a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="84a1a-119">Remarks</span></span>

<span data-ttu-id="84a1a-120">Ogni valore nella matrice a cui punta il *PID* è una delle [costanti della proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="84a1a-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="84a1a-121">È possibile estendere questo sistema di identificazione.</span><span class="sxs-lookup"><span data-stu-id="84a1a-121">You can extend this identification system.</span></span> <span data-ttu-id="84a1a-122">Vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="84a1a-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="84a1a-123">Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="84a1a-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="84a1a-124">Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.</span><span class="sxs-lookup"><span data-stu-id="84a1a-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a1a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84a1a-125">Requirements</span></span>



| <span data-ttu-id="84a1a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a1a-126">Requirement</span></span> | <span data-ttu-id="84a1a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="84a1a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a1a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="84a1a-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84a1a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="84a1a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="84a1a-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84a1a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84a1a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84a1a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a1a-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a1a-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="84a1a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="84a1a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84a1a-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84a1a-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a1a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84a1a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a1a-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="84a1a-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="84a1a-138">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="84a1a-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="84a1a-139">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="84a1a-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="84a1a-140">Costanti della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="84a1a-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="84a1a-141">Definizione di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="84a1a-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




