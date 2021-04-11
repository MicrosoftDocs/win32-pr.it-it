---
description: Ottiene il numero di profili di analisi per il dispositivo.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Metodo IScanProfileMgr:: GetNumProfilesforDeviceID (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226324"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="44676-103">Metodo IScanProfileMgr:: GetNumProfilesforDeviceID</span><span class="sxs-lookup"><span data-stu-id="44676-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="44676-104">Ottiene il numero di profili di analisi per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44676-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="44676-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44676-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="44676-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="44676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44676-107">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44676-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44676-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="44676-108">Type: **BSTR**</span></span>

<span data-ttu-id="44676-109">ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44676-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="44676-110">*pulNumProfiles* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="44676-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44676-111">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="44676-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="44676-112">Puntatore al numero di profili disponibili per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44676-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44676-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44676-113">Return value</span></span>

<span data-ttu-id="44676-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="44676-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="44676-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="44676-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44676-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44676-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44676-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44676-117">Requirements</span></span>



| <span data-ttu-id="44676-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="44676-118">Requirement</span></span> | <span data-ttu-id="44676-119">Valore</span><span class="sxs-lookup"><span data-stu-id="44676-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="44676-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44676-120">Minimum supported client</span></span><br/> | <span data-ttu-id="44676-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44676-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="44676-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44676-122">Minimum supported server</span></span><br/> | <span data-ttu-id="44676-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44676-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44676-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44676-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="44676-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="44676-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="44676-126">IDL</span><span class="sxs-lookup"><span data-stu-id="44676-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44676-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44676-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44676-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44676-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44676-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="44676-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="44676-130">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="44676-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




