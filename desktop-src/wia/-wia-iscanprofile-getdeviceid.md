---
description: Restituisce l'ID del dispositivo.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'Metodo IScanProfile:: GetDeviceID (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344016"
---
# <a name="iscanprofilegetdeviceid-method"></a><span data-ttu-id="75706-103">Metodo IScanProfile:: GetDeviceID</span><span class="sxs-lookup"><span data-stu-id="75706-103">IScanProfile::GetDeviceID method</span></span>

<span data-ttu-id="75706-104">Restituisce l'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75706-104">Returns the ID of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="75706-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75706-105">Syntax</span></span>


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="75706-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75706-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75706-107">*pbstrDeviceID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="75706-107">*pbstrDeviceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75706-108">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="75706-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="75706-109">Puntatore all'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75706-109">A pointer to the device ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75706-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75706-110">Return value</span></span>

<span data-ttu-id="75706-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="75706-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="75706-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="75706-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75706-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75706-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="75706-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75706-114">Requirements</span></span>



| <span data-ttu-id="75706-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="75706-115">Requirement</span></span> | <span data-ttu-id="75706-116">Valore</span><span class="sxs-lookup"><span data-stu-id="75706-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="75706-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75706-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75706-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75706-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="75706-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75706-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75706-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75706-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75706-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75706-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="75706-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="75706-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="75706-123">IDL</span><span class="sxs-lookup"><span data-stu-id="75706-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75706-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75706-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75706-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75706-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75706-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="75706-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="75706-127">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="75706-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




