---
title: Messaggio CQPM_HANDLERSPECIFIC (cmnquery. h)
description: Valore di base utilizzato per i messaggi privati del gestore di query.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475586"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="6b552-104">\_Messaggio CQPM HANDLERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="6b552-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="6b552-105">Il **messaggio \_ HANDLERSPECIFIC di CQPM** è il valore di base utilizzato per i messaggi privati del gestore di query.</span><span class="sxs-lookup"><span data-stu-id="6b552-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="6b552-106">Il gestore di query deve aggiungere questo valore ai messaggi privati per assicurarsi che non si verifichino conflitti di messaggi.</span><span class="sxs-lookup"><span data-stu-id="6b552-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b552-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b552-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b552-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b552-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b552-109">Contiene dati aggiuntivi del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6b552-109">Contains additional message data.</span></span> <span data-ttu-id="6b552-110">Il contenuto di questo parametro è definito dal gestore di query.</span><span class="sxs-lookup"><span data-stu-id="6b552-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="6b552-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b552-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b552-112">Contiene dati aggiuntivi del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6b552-112">Contains additional message data.</span></span> <span data-ttu-id="6b552-113">Il contenuto di questo parametro è definito dal gestore di query.</span><span class="sxs-lookup"><span data-stu-id="6b552-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b552-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b552-114">Return value</span></span>

<span data-ttu-id="6b552-115">Il significato del valore restituito è definito dal gestore di query.</span><span class="sxs-lookup"><span data-stu-id="6b552-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b552-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b552-116">Requirements</span></span>



| <span data-ttu-id="6b552-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b552-117">Requirement</span></span> | <span data-ttu-id="6b552-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6b552-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b552-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b552-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b552-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b552-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="6b552-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b552-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b552-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b552-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="6b552-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b552-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b552-124"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b552-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b552-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b552-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b552-126">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="6b552-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





