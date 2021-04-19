---
description: Crea un profilo di analisi vuoto e lo associa a uno scanner o ad altro elemento Windows Image Acquisition (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Metodo IScanProfileMgr:: CreateProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485293"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="1b99f-103">Metodo IScanProfileMgr:: CreateProfile</span><span class="sxs-lookup"><span data-stu-id="1b99f-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="1b99f-104">Crea un profilo di analisi vuoto e lo associa a uno scanner o ad altro elemento Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="1b99f-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b99f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b99f-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="1b99f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b99f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b99f-107">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-108">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-109">ID del dispositivo o dell'elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="1b99f-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-111">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b99f-111">Type: **BSTR**</span></span>

<span data-ttu-id="1b99f-112">Nome descrittivo del nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="1b99f-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-113">*guidCategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-114">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="1b99f-114">Type: **GUID**</span></span>

<span data-ttu-id="1b99f-115">GUID della categoria del dispositivo o dell'elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="1b99f-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="1b99f-116">Deve corrispondere a una delle costanti di \_ categoria degli elementi dell'IPA WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b99f-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="1b99f-117">*ppScanProfile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99f-118">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1b99f-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="1b99f-119">Indirizzo di un puntatore al nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="1b99f-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b99f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b99f-120">Return value</span></span>

<span data-ttu-id="1b99f-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b99f-121">Type: **HRESULT**</span></span>

<span data-ttu-id="1b99f-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1b99f-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b99f-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b99f-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b99f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b99f-124">Remarks</span></span>

<span data-ttu-id="1b99f-125">**IScanProfileMgr:: CreateProfile** associa il dispositivo specificato al nuovo profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="1b99f-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="1b99f-126">**IScanProfileMgr:: CreateProfile** genera automaticamente un GUID per il nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="1b99f-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="1b99f-127">Ottenere il GUID con [**GetGuid**](-wia-iscanprofile-getguid.md).</span><span class="sxs-lookup"><span data-stu-id="1b99f-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="1b99f-128">Usare il metodo [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando è possibile che più di un oggetto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) crei o elimini i profili nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="1b99f-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b99f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b99f-129">Requirements</span></span>



| <span data-ttu-id="1b99f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b99f-130">Requirement</span></span> | <span data-ttu-id="1b99f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1b99f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b99f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b99f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1b99f-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1b99f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b99f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1b99f-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b99f-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b99f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b99f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b99f-137"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b99f-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="1b99f-138">IDL</span><span class="sxs-lookup"><span data-stu-id="1b99f-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b99f-139"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b99f-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b99f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b99f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b99f-141">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="1b99f-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="1b99f-142">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="1b99f-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




