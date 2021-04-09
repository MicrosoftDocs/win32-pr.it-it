---
description: Elimina tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: Metodo IScanProfileMgr::D eleteAllProfilesForUser (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130023"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="e457e-103">IScanProfileMgr::D Metodo eleteAllProfilesForUser</span><span class="sxs-lookup"><span data-stu-id="e457e-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="e457e-104">Elimina tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e457e-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="e457e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e457e-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="e457e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e457e-106">Parameters</span></span>

<span data-ttu-id="e457e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e457e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e457e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e457e-108">Return value</span></span>

<span data-ttu-id="e457e-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e457e-109">Type: **HRESULT**</span></span>

<span data-ttu-id="e457e-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e457e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e457e-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e457e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e457e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e457e-112">Requirements</span></span>



| <span data-ttu-id="e457e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e457e-113">Requirement</span></span> | <span data-ttu-id="e457e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e457e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e457e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e457e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e457e-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e457e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e457e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e457e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e457e-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e457e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e457e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e457e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e457e-120"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e457e-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="e457e-121">IDL</span><span class="sxs-lookup"><span data-stu-id="e457e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e457e-122"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e457e-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e457e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e457e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e457e-124">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="e457e-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="e457e-125">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="e457e-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




