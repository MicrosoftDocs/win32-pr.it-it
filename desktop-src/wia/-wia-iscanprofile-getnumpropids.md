---
description: Ottiene il numero di ID di proprietà in un profilo.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'Metodo IScanProfile:: GetNumPropIDS (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130030"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="4e011-103">Metodo IScanProfile:: GetNumPropIDS</span><span class="sxs-lookup"><span data-stu-id="4e011-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="4e011-104">Ottiene il numero di ID di proprietà in un profilo.</span><span class="sxs-lookup"><span data-stu-id="4e011-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e011-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e011-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="4e011-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e011-107">numero di  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e011-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e011-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="4e011-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="4e011-109">Numero di ID di proprietà nel profilo.</span><span class="sxs-lookup"><span data-stu-id="4e011-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e011-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e011-110">Return value</span></span>

<span data-ttu-id="4e011-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4e011-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4e011-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4e011-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e011-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e011-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e011-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e011-114">Requirements</span></span>



| <span data-ttu-id="4e011-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e011-115">Requirement</span></span> | <span data-ttu-id="4e011-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4e011-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e011-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e011-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4e011-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e011-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4e011-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e011-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4e011-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e011-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e011-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e011-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e011-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e011-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="4e011-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4e011-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e011-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e011-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e011-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e011-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e011-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="4e011-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="4e011-127">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="4e011-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




