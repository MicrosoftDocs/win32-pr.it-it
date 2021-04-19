---
description: Ottiene il numero di profili di analisi creati per l'utente nel sistema in cui viene eseguita l'applicazione.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Metodo IScanProfileMgr:: GetNumProfiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312431"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="f065e-103">Metodo IScanProfileMgr:: GetNumProfiles</span><span class="sxs-lookup"><span data-stu-id="f065e-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="f065e-104">Ottiene il numero di profili di analisi creati per l'utente nel sistema in cui viene eseguita l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f065e-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="f065e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f065e-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="f065e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f065e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f065e-107">*pulNumProfiles* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f065e-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f065e-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="f065e-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="f065e-109">Puntatore al numero di profili creati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="f065e-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f065e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f065e-110">Return value</span></span>

<span data-ttu-id="f065e-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f065e-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f065e-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f065e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f065e-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f065e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f065e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f065e-114">Requirements</span></span>



| <span data-ttu-id="f065e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f065e-115">Requirement</span></span> | <span data-ttu-id="f065e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f065e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f065e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f065e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f065e-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f065e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f065e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f065e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f065e-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f065e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f065e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f065e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f065e-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f065e-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="f065e-123">IDL</span><span class="sxs-lookup"><span data-stu-id="f065e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f065e-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f065e-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f065e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f065e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f065e-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="f065e-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="f065e-127">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="f065e-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




