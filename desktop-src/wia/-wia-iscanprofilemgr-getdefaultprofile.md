---
description: Ottiene il profilo di analisi predefinito.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'Metodo IScanProfileMgr:: GetDefaultProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e058094fc29510d6e073abc0b05374403a2b5cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308257"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a><span data-ttu-id="17cb5-103">Metodo IScanProfileMgr:: GetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17cb5-103">IScanProfileMgr::GetDefaultProfile method</span></span>

<span data-ttu-id="17cb5-104">Ottiene il profilo di analisi predefinito.</span><span class="sxs-lookup"><span data-stu-id="17cb5-104">Gets the default scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="17cb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17cb5-105">Syntax</span></span>


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="17cb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17cb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17cb5-107">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17cb5-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17cb5-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="17cb5-108">Type: **BSTR**</span></span>

<span data-ttu-id="17cb5-109">ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17cb5-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="17cb5-110">*ppScanProfile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17cb5-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17cb5-111">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="17cb5-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="17cb5-112">Indirizzo di un puntatore al profilo predefinito del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17cb5-112">The address of a pointer to the device's default profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17cb5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17cb5-113">Return value</span></span>

<span data-ttu-id="17cb5-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="17cb5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="17cb5-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17cb5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17cb5-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17cb5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17cb5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="17cb5-117">Remarks</span></span>

<span data-ttu-id="17cb5-118">Il profilo predefinito contiene un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="17cb5-118">The default profile has a `<Default>` element.</span></span>

## <a name="requirements"></a><span data-ttu-id="17cb5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17cb5-119">Requirements</span></span>



| <span data-ttu-id="17cb5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="17cb5-120">Requirement</span></span> | <span data-ttu-id="17cb5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="17cb5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="17cb5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17cb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="17cb5-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17cb5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="17cb5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17cb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="17cb5-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17cb5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17cb5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17cb5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="17cb5-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="17cb5-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="17cb5-128">IDL</span><span class="sxs-lookup"><span data-stu-id="17cb5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17cb5-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17cb5-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17cb5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17cb5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17cb5-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="17cb5-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="17cb5-132">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="17cb5-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




