---
description: Elimina il profilo di analisi specificato.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: Metodo IScanProfileMgr::D eleteProfile (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967574"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="f1444-103">IScanProfileMgr::D Metodo eleteProfile</span><span class="sxs-lookup"><span data-stu-id="f1444-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="f1444-104">Elimina il profilo di analisi specificato.</span><span class="sxs-lookup"><span data-stu-id="f1444-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1444-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1444-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="f1444-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1444-107">*pScanProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1444-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1444-108">Tipo: \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f1444-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="f1444-109">Puntatore al profilo.</span><span class="sxs-lookup"><span data-stu-id="f1444-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1444-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1444-110">Return value</span></span>

<span data-ttu-id="f1444-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f1444-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f1444-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f1444-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1444-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1444-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1444-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1444-114">Remarks</span></span>

<span data-ttu-id="f1444-115">**IScanProfileMgr::D eleteprofile** Elimina il profilo dal disco ed Elimina l'oggetto profilo in memoria.</span><span class="sxs-lookup"><span data-stu-id="f1444-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="f1444-116">Usare il metodo [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando è possibile che più di un oggetto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) crei o elimini i profili nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="f1444-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1444-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1444-117">Requirements</span></span>



| <span data-ttu-id="f1444-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1444-118">Requirement</span></span> | <span data-ttu-id="f1444-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f1444-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1444-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1444-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1444-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1444-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f1444-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1444-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1444-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1444-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1444-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1444-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1444-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1444-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="f1444-126">IDL</span><span class="sxs-lookup"><span data-stu-id="f1444-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1444-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1444-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1444-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1444-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1444-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="f1444-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="f1444-130">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="f1444-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




