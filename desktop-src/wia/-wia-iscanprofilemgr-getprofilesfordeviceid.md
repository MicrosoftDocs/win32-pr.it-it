---
description: Ottiene tutti i profili di analisi associati a un dispositivo.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Metodo IScanProfileMgr:: GetProfilesforDeviceID (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308251"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="77616-103">Metodo IScanProfileMgr:: GetProfilesforDeviceID</span><span class="sxs-lookup"><span data-stu-id="77616-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="77616-104">Ottiene tutti i profili di analisi associati a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77616-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="77616-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77616-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="77616-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="77616-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77616-107">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77616-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77616-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="77616-108">Type: **BSTR**</span></span>

<span data-ttu-id="77616-109">ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77616-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="77616-110">*pulNumProfiles* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="77616-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77616-111">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="77616-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="77616-112">Quando viene passato, un puntatore al numero massimo di profili da restituire.</span><span class="sxs-lookup"><span data-stu-id="77616-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="77616-113">Quando viene restituito, il puntatore al numero di profili restituiti.</span><span class="sxs-lookup"><span data-stu-id="77616-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="77616-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77616-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77616-115">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="77616-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="77616-116">Indirizzo di un puntatore a una matrice di profili.</span><span class="sxs-lookup"><span data-stu-id="77616-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77616-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77616-117">Return value</span></span>

<span data-ttu-id="77616-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="77616-118">Type: **HRESULT**</span></span>

<span data-ttu-id="77616-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="77616-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77616-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77616-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77616-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="77616-121">Remarks</span></span>

<span data-ttu-id="77616-122">Se il numero totale di profili associati al dispositivo è inferiore al valore passato a *pulNumProfiles*, *pulNumProfiles* restituisce il totale.</span><span class="sxs-lookup"><span data-stu-id="77616-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="77616-123">In caso contrario, restituisce lo stesso valore che è stato passato.</span><span class="sxs-lookup"><span data-stu-id="77616-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="77616-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77616-124">Requirements</span></span>



| <span data-ttu-id="77616-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="77616-125">Requirement</span></span> | <span data-ttu-id="77616-126">Valore</span><span class="sxs-lookup"><span data-stu-id="77616-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="77616-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77616-127">Minimum supported client</span></span><br/> | <span data-ttu-id="77616-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77616-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="77616-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77616-129">Minimum supported server</span></span><br/> | <span data-ttu-id="77616-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77616-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77616-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77616-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="77616-132"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="77616-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="77616-133">IDL</span><span class="sxs-lookup"><span data-stu-id="77616-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77616-134"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77616-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77616-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77616-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77616-136">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="77616-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="77616-137">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="77616-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




