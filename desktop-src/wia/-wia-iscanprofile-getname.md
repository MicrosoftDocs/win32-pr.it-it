---
description: Ottiene il nome descrittivo del profilo.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'Metodo IScanProfile:: GetName (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226326"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="18a0b-103">Metodo IScanProfile:: GetName</span><span class="sxs-lookup"><span data-stu-id="18a0b-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="18a0b-104">Ottiene il nome descrittivo del profilo.</span><span class="sxs-lookup"><span data-stu-id="18a0b-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a0b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18a0b-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="18a0b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18a0b-107">*pbstrName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="18a0b-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18a0b-108">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="18a0b-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="18a0b-109">Nome descrittivo del profilo.</span><span class="sxs-lookup"><span data-stu-id="18a0b-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18a0b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18a0b-110">Return value</span></span>

<span data-ttu-id="18a0b-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="18a0b-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="18a0b-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="18a0b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18a0b-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18a0b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18a0b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="18a0b-114">Remarks</span></span>

<span data-ttu-id="18a0b-115">Questo metodo è necessario perché non è possibile usare il GUID di un profilo per visualizzare il profilo di analisi a un utente.</span><span class="sxs-lookup"><span data-stu-id="18a0b-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="18a0b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18a0b-116">Requirements</span></span>



| <span data-ttu-id="18a0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a0b-117">Requirement</span></span> | <span data-ttu-id="18a0b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="18a0b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a0b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18a0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18a0b-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18a0b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="18a0b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18a0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18a0b-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18a0b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18a0b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18a0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18a0b-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="18a0b-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="18a0b-125">IDL</span><span class="sxs-lookup"><span data-stu-id="18a0b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18a0b-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18a0b-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a0b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18a0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a0b-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="18a0b-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="18a0b-129">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="18a0b-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




