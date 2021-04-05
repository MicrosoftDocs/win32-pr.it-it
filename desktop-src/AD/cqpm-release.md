---
title: Messaggio CQPM_RELEASE (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query quando la pagina sta per essere scaricata.
ms.assetid: b935ae8d-a07f-4f0d-b379-5512e96a25a5
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_RELEASE Active Directory
topic_type:
- apiref
api_name:
- CQPM_RELEASE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4957f02b57f499d80f7802b4fe9bd2639485b8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048306"
---
# <a name="cqpm_release-message"></a><span data-ttu-id="f76cb-104">\_Messaggio di rilascio CQPM</span><span class="sxs-lookup"><span data-stu-id="f76cb-104">CQPM\_RELEASE message</span></span>

<span data-ttu-id="f76cb-105">Il messaggio della **\_ versione CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query quando la pagina sta per essere scaricata.</span><span class="sxs-lookup"><span data-stu-id="f76cb-105">The **CQPM\_RELEASE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is about to be unloaded.</span></span>

## <a name="parameters"></a><span data-ttu-id="f76cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f76cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f76cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f76cb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f76cb-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f76cb-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f76cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f76cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f76cb-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f76cb-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f76cb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f76cb-111">Return value</span></span>

<span data-ttu-id="f76cb-112">Il valore restituito per questo messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f76cb-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f76cb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f76cb-113">Requirements</span></span>



| <span data-ttu-id="f76cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f76cb-114">Requirement</span></span> | <span data-ttu-id="f76cb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f76cb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f76cb-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f76cb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f76cb-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f76cb-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f76cb-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f76cb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f76cb-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f76cb-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f76cb-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f76cb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f76cb-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="f76cb-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f76cb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f76cb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76cb-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="f76cb-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





