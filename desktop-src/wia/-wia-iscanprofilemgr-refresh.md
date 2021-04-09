---
description: Enumera nuovamente tutti i profili di analisi nel sistema.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'Metodo IScanProfileMgr:: Refresh (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966839"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="d69e0-103">Metodo IScanProfileMgr:: Refresh</span><span class="sxs-lookup"><span data-stu-id="d69e0-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="d69e0-104">Enumera nuovamente tutti i profili di analisi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d69e0-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d69e0-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="d69e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d69e0-106">Parameters</span></span>

<span data-ttu-id="d69e0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d69e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d69e0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d69e0-108">Return value</span></span>

<span data-ttu-id="d69e0-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d69e0-109">Type: **HRESULT**</span></span>

<span data-ttu-id="d69e0-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d69e0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d69e0-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d69e0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d69e0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d69e0-112">Remarks</span></span>

<span data-ttu-id="d69e0-113">Utilizzare questo metodo quando è possibile che più di un oggetto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) crei o elimini profili nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="d69e0-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69e0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d69e0-114">Requirements</span></span>



| <span data-ttu-id="d69e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d69e0-115">Requirement</span></span> | <span data-ttu-id="d69e0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d69e0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69e0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d69e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d69e0-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d69e0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d69e0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d69e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d69e0-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d69e0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d69e0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d69e0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69e0-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69e0-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="d69e0-123">IDL</span><span class="sxs-lookup"><span data-stu-id="d69e0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d69e0-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d69e0-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d69e0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d69e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69e0-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="d69e0-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="d69e0-127">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="d69e0-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




