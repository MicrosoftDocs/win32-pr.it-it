---
description: Restituisce il GUID del profilo.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'Metodo IScanProfile:: GetGuid (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344011"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="6f720-103">Metodo IScanProfile:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="6f720-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="6f720-104">Restituisce il GUID del profilo.</span><span class="sxs-lookup"><span data-stu-id="6f720-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f720-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f720-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="6f720-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f720-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f720-107">*retval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6f720-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f720-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="6f720-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="6f720-109">Puntatore al GUID del profilo.</span><span class="sxs-lookup"><span data-stu-id="6f720-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f720-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f720-110">Return value</span></span>

<span data-ttu-id="6f720-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6f720-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6f720-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f720-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f720-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f720-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f720-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f720-114">Remarks</span></span>

<span data-ttu-id="6f720-115">Il GUID di un profilo viene generato automaticamente quando il profilo viene creato con [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span><span class="sxs-lookup"><span data-stu-id="6f720-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f720-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f720-116">Requirements</span></span>



| <span data-ttu-id="6f720-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f720-117">Requirement</span></span> | <span data-ttu-id="6f720-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6f720-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f720-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f720-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f720-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f720-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6f720-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f720-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f720-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f720-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f720-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f720-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f720-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f720-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="6f720-125">IDL</span><span class="sxs-lookup"><span data-stu-id="6f720-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f720-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f720-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f720-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f720-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f720-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="6f720-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="6f720-129">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="6f720-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




