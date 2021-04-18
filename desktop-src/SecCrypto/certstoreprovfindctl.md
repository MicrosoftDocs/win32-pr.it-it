---
description: Enumera o trova il primo o il CTL successivo in un archivio esterno che corrisponde ai criteri specificati.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Funzione di callback CertStoreProvFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315806"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="52ab3-103">Funzione di callback CertStoreProvFindCTL</span><span class="sxs-lookup"><span data-stu-id="52ab3-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="52ab3-104">La funzione di callback **CertStoreProvFindCTL** enumera o trova il primo o il successivo [*CTL*](../secgloss/c-gly.md) in un [*archivio esterno*](../secgloss/e-gly.md) che corrisponde ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="52ab3-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ab3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52ab3-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="52ab3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52ab3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ab3-107">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ab3-108">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="52ab3-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="52ab3-109">*pFindInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ab3-110">Un puntatore a un [**\_ archivio certificati \_ prova a \_ trovare \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la struttura di informazioni contenente tutti i parametri passati a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="52ab3-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="52ab3-111">CHANGETABLE(CHANGES …).</span><span class="sxs-lookup"><span data-stu-id="52ab3-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="52ab3-112">*pPrevCtlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ab3-113">Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) dell'ultimo CTL trovato.</span><span class="sxs-lookup"><span data-stu-id="52ab3-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="52ab3-114">Alla prima chiamata alla funzione, questo parametro deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="52ab3-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="52ab3-115">Nelle chiamate successive deve essere impostato sul puntatore restituito nel parametro *ppProvCTLContext* nell'ultima chiamata.</span><span class="sxs-lookup"><span data-stu-id="52ab3-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="52ab3-116">Un puntatore non **null** passato in questo parametro viene liberato dalla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="52ab3-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="52ab3-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ab3-118">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="52ab3-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="52ab3-119">*ppvStoreProvFindInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ab3-120">Puntatore a un puntatore al buffer per restituire le informazioni sul provider dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="52ab3-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="52ab3-121">Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="52ab3-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="52ab3-122">Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.</span><span class="sxs-lookup"><span data-stu-id="52ab3-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="52ab3-123">*ppProvCtlContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ab3-124">In una ricerca riuscita viene restituito un puntatore al CTL trovato in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="52ab3-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ab3-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52ab3-125">Return value</span></span>

<span data-ttu-id="52ab3-126">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="52ab3-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="52ab3-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52ab3-127">Requirements</span></span>



| <span data-ttu-id="52ab3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ab3-128">Requirement</span></span> | <span data-ttu-id="52ab3-129">Valore</span><span class="sxs-lookup"><span data-stu-id="52ab3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52ab3-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52ab3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="52ab3-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="52ab3-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52ab3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="52ab3-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52ab3-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52ab3-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52ab3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ab3-135">**\_informazioni su \_ prova \_ archivio \_ certificati**</span><span class="sxs-lookup"><span data-stu-id="52ab3-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="52ab3-136">**CertFindCTLInStore**</span><span class="sxs-lookup"><span data-stu-id="52ab3-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="52ab3-137">**\_contesto CTL**</span><span class="sxs-lookup"><span data-stu-id="52ab3-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
