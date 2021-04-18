---
description: Ottiene tutti gli ID di proprietà disponibili in un profilo.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Metodo IScanProfile:: GetAllPropIDs (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308265"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="5a07c-103">Metodo IScanProfile:: GetAllPropIDs</span><span class="sxs-lookup"><span data-stu-id="5a07c-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="5a07c-104">Ottiene tutti gli ID di proprietà disponibili in un profilo.</span><span class="sxs-lookup"><span data-stu-id="5a07c-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a07c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a07c-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="5a07c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a07c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a07c-107">numero di  \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5a07c-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a07c-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="5a07c-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="5a07c-109">Numero di ID di proprietà richiesti o restituiti.</span><span class="sxs-lookup"><span data-stu-id="5a07c-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="5a07c-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a07c-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a07c-111">Tipo: \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="5a07c-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="5a07c-112">Puntatore a una matrice di ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a07c-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a07c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a07c-113">Return value</span></span>

<span data-ttu-id="5a07c-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5a07c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5a07c-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a07c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a07c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a07c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a07c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a07c-117">Requirements</span></span>



| <span data-ttu-id="5a07c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a07c-118">Requirement</span></span> | <span data-ttu-id="5a07c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5a07c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a07c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a07c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a07c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a07c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5a07c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a07c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a07c-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a07c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a07c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a07c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a07c-125"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a07c-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="5a07c-126">IDL</span><span class="sxs-lookup"><span data-stu-id="5a07c-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a07c-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a07c-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a07c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a07c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a07c-129">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="5a07c-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="5a07c-130">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="5a07c-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




