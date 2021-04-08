---
title: Messaggio CQPM_ENABLE (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per abilitare o disabilitare la pagina.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048003"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="967c8-104">\_Messaggio di abilitazione CQPM</span><span class="sxs-lookup"><span data-stu-id="967c8-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="967c8-105">Il messaggio di **\_ Abilitazione di CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per abilitare o disabilitare la pagina.</span><span class="sxs-lookup"><span data-stu-id="967c8-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="967c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="967c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="967c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="967c8-108">Contiene zero per disabilitare la pagina o un valore diverso da zero per abilitare la pagina.</span><span class="sxs-lookup"><span data-stu-id="967c8-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="967c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="967c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="967c8-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="967c8-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967c8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="967c8-111">Return value</span></span>

<span data-ttu-id="967c8-112">Il valore restituito per questo messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="967c8-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="967c8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="967c8-113">Requirements</span></span>



| <span data-ttu-id="967c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="967c8-114">Requirement</span></span> | <span data-ttu-id="967c8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="967c8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="967c8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="967c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="967c8-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="967c8-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="967c8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="967c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="967c8-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="967c8-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="967c8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="967c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="967c8-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="967c8-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967c8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="967c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967c8-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="967c8-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





