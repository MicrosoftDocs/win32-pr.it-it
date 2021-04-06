---
title: Messaggio CQPM_GETPARAMETERS (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per recuperare i dati relativi alla query eseguita dalla pagina.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_GETPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873441"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="0a29a-104">\_Messaggio GETparameters CQPM</span><span class="sxs-lookup"><span data-stu-id="0a29a-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="0a29a-105">Il messaggio **CQPM \_ GetParameters** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per recuperare i dati relativi alla query eseguita dalla pagina.</span><span class="sxs-lookup"><span data-stu-id="0a29a-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a29a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a29a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a29a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a29a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a29a-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="0a29a-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0a29a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a29a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a29a-110">Puntatore a un valore [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) che riceve i dati relativi alla query eseguita dalla pagina.</span><span class="sxs-lookup"><span data-stu-id="0a29a-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="0a29a-111">Se questo parametro è **null**, la struttura **DSQUERYPARAMS** deve essere allocata dall'estensione utilizzando la funzione [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .</span><span class="sxs-lookup"><span data-stu-id="0a29a-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a29a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a29a-112">Return value</span></span>

<span data-ttu-id="0a29a-113">Restituisce **\_ OK** se l'esito è positivo o un codice di errore **HRESULT** standard.</span><span class="sxs-lookup"><span data-stu-id="0a29a-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a29a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a29a-114">Requirements</span></span>



| <span data-ttu-id="0a29a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a29a-115">Requirement</span></span> | <span data-ttu-id="0a29a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0a29a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a29a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a29a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a29a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a29a-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="0a29a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a29a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a29a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a29a-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="0a29a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a29a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a29a-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a29a-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a29a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a29a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a29a-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="0a29a-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="0a29a-125">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="0a29a-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="0a29a-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="0a29a-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

