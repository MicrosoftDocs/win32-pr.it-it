---
title: Messaggio CQPM_SETDEFAULTPARAMETERS (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per impostare parametri predefiniti alternativi per la pagina.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476492"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="53e1b-104">\_Messaggio CQPM SETDEFAULTPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53e1b-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="53e1b-105">Il messaggio **CQPM \_ SETDEFAULTPARAMETERS** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per impostare parametri predefiniti alternativi per la pagina.</span><span class="sxs-lookup"><span data-stu-id="53e1b-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="53e1b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53e1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e1b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53e1b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53e1b-108">Contiene un valore diverso da zero se la pagina è la pagina predefinita o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="53e1b-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="53e1b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53e1b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53e1b-110">Puntatore a una struttura [**openQueryWindow**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) che contiene i dati sulla finestra di dialogo query del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="53e1b-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e1b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53e1b-111">Return value</span></span>

<span data-ttu-id="53e1b-112">Il valore restituito per questo messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="53e1b-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e1b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53e1b-113">Requirements</span></span>



| <span data-ttu-id="53e1b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e1b-114">Requirement</span></span> | <span data-ttu-id="53e1b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="53e1b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53e1b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e1b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53e1b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53e1b-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="53e1b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e1b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53e1b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53e1b-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="53e1b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53e1b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53e1b-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="53e1b-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e1b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53e1b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e1b-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="53e1b-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="53e1b-124">**OPENQUERYWINDOW**</span><span class="sxs-lookup"><span data-stu-id="53e1b-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





