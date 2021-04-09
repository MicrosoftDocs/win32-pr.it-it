---
description: Elimina tutti i profili di analisi associati al dispositivo specificato.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: Metodo IScanProfileMgr::D eleteAllProfiles (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050037"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="d34c8-103">IScanProfileMgr::D Metodo eleteAllProfiles</span><span class="sxs-lookup"><span data-stu-id="d34c8-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="d34c8-104">Elimina tutti i profili di analisi associati al dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="d34c8-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d34c8-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="d34c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d34c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34c8-107">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34c8-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34c8-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d34c8-108">Type: **BSTR**</span></span>

<span data-ttu-id="d34c8-109">ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d34c8-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34c8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d34c8-110">Return value</span></span>

<span data-ttu-id="d34c8-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d34c8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d34c8-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d34c8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d34c8-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d34c8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d34c8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d34c8-114">Requirements</span></span>



| <span data-ttu-id="d34c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34c8-115">Requirement</span></span> | <span data-ttu-id="d34c8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d34c8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34c8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d34c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d34c8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d34c8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d34c8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d34c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d34c8-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d34c8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d34c8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d34c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d34c8-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34c8-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="d34c8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="d34c8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d34c8-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d34c8-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34c8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d34c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34c8-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="d34c8-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="d34c8-127">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="d34c8-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




