---
description: Apre un profilo di analisi salvato su disco come file XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'Metodo IScanProfileMgr:: OpenProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312430"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="7f908-103">Metodo IScanProfileMgr:: OpenProfile</span><span class="sxs-lookup"><span data-stu-id="7f908-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="7f908-104">Apre un profilo di analisi salvato su disco come file XML.</span><span class="sxs-lookup"><span data-stu-id="7f908-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f908-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f908-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="7f908-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f908-107">*GUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f908-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f908-108">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="7f908-108">Type: **GUID**</span></span>

<span data-ttu-id="7f908-109">GUID del profilo.</span><span class="sxs-lookup"><span data-stu-id="7f908-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="7f908-110">*ppScanProfile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f908-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f908-111">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7f908-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="7f908-112">Indirizzo di un puntatore al profilo.</span><span class="sxs-lookup"><span data-stu-id="7f908-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f908-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f908-113">Return value</span></span>

<span data-ttu-id="7f908-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f908-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7f908-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7f908-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f908-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f908-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f908-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f908-117">Remarks</span></span>

<span data-ttu-id="7f908-118">Se un profilo di analisi viene salvato utilizzando il metodo [**Save**](-wia-iscanprofile-save.md) , viene archiviato come file XML in% UserProfile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="7f908-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f908-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f908-119">Requirements</span></span>



| <span data-ttu-id="7f908-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f908-120">Requirement</span></span> | <span data-ttu-id="7f908-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7f908-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f908-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f908-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f908-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f908-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7f908-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f908-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f908-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f908-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f908-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f908-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f908-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f908-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="7f908-128">IDL</span><span class="sxs-lookup"><span data-stu-id="7f908-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f908-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f908-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f908-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f908-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f908-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="7f908-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="7f908-132">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="7f908-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




