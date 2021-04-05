---
description: Ottiene tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Metodo IScanProfileMgr:: GetProfiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756644"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="60dbd-103">Metodo IScanProfileMgr:: GetProfiles</span><span class="sxs-lookup"><span data-stu-id="60dbd-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="60dbd-104">Ottiene tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60dbd-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="60dbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60dbd-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="60dbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60dbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60dbd-107">*pulNumProfiles* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="60dbd-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60dbd-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="60dbd-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="60dbd-109">Quando viene passato, un puntatore al numero massimo di profili da restituire.</span><span class="sxs-lookup"><span data-stu-id="60dbd-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="60dbd-110">Quando viene restituito, un puntatore al numero di profili restituiti.</span><span class="sxs-lookup"><span data-stu-id="60dbd-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="60dbd-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60dbd-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60dbd-112">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="60dbd-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="60dbd-113">Indirizzo di una matrice di puntatori ai profili.</span><span class="sxs-lookup"><span data-stu-id="60dbd-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60dbd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60dbd-114">Return value</span></span>

<span data-ttu-id="60dbd-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="60dbd-115">Type: **HRESULT**</span></span>

<span data-ttu-id="60dbd-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="60dbd-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60dbd-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60dbd-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="60dbd-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="60dbd-118">Remarks</span></span>

<span data-ttu-id="60dbd-119">Se il numero totale di profili disponibili per l'utente è inferiore al valore passato a *pulNumProfiles*, *pulNumProfiles* restituisce il totale.</span><span class="sxs-lookup"><span data-stu-id="60dbd-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="60dbd-120">In caso contrario, restituisce lo stesso valore che è stato passato.</span><span class="sxs-lookup"><span data-stu-id="60dbd-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="60dbd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60dbd-121">Requirements</span></span>



| <span data-ttu-id="60dbd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="60dbd-122">Requirement</span></span> | <span data-ttu-id="60dbd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="60dbd-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60dbd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60dbd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60dbd-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60dbd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="60dbd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60dbd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60dbd-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60dbd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60dbd-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60dbd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="60dbd-129"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="60dbd-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="60dbd-130">IDL</span><span class="sxs-lookup"><span data-stu-id="60dbd-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60dbd-131"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60dbd-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60dbd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60dbd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60dbd-133">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="60dbd-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="60dbd-134">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="60dbd-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




