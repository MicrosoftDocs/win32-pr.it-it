---
title: Messaggio CQPM_INITIALIZE (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query quando la pagina viene aggiunta a un modulo.
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_INITIALIZE Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048308"
---
# <a name="cqpm_initialize-message"></a><span data-ttu-id="49afc-104">\_Messaggio di inizializzazione CQPM</span><span class="sxs-lookup"><span data-stu-id="49afc-104">CQPM\_INITIALIZE message</span></span>

<span data-ttu-id="49afc-105">Il messaggio di **\_ inizializzazione CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query quando la pagina viene aggiunta a un modulo.</span><span class="sxs-lookup"><span data-stu-id="49afc-105">The **CQPM\_INITIALIZE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is added to a form.</span></span>

## <a name="parameters"></a><span data-ttu-id="49afc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49afc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49afc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49afc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49afc-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="49afc-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="49afc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49afc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49afc-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="49afc-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49afc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49afc-111">Return value</span></span>

<span data-ttu-id="49afc-112">Il valore restituito per questo messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="49afc-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="49afc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49afc-113">Requirements</span></span>



| <span data-ttu-id="49afc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49afc-114">Requirement</span></span> | <span data-ttu-id="49afc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49afc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49afc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49afc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49afc-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49afc-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="49afc-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49afc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49afc-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49afc-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="49afc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49afc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49afc-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="49afc-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49afc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49afc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49afc-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="49afc-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





