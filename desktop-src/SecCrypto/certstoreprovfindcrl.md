---
description: Enumera o trova il primo o il CRL successivo in un archivio esterno che corrisponde ai criteri specificati.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Funzione di callback CertStoreProvFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529712"
---
# <a name="certstoreprovfindcrl-callback-function"></a><span data-ttu-id="e4e5f-103">Funzione di callback CertStoreProvFindCRL</span><span class="sxs-lookup"><span data-stu-id="e4e5f-103">CertStoreProvFindCRL callback function</span></span>

<span data-ttu-id="e4e5f-104">La funzione di callback **CertStoreProvFindCRL** enumera o trova il primo o il [*CRL*](../secgloss/c-gly.md) successivo in un [*Archivio*](../secgloss/e-gly.md) esterno che corrisponde ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-104">The **CertStoreProvFindCRL** callback function enumerates or finds the first or next [*CRL*](../secgloss/c-gly.md) in an external [*store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4e5f-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
);
```



## <a name="parameters"></a><span data-ttu-id="e4e5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4e5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e5f-107">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5f-108">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e4e5f-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e5f-109">*pFindInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5f-110">Un puntatore a un [**\_ archivio certificati \_ prova a \_ trovare \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la struttura di informazioni contenente tutti i parametri passati alla funzione [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .</span><span class="sxs-lookup"><span data-stu-id="e4e5f-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="e4e5f-111">*pPrevCrlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-111">*pPrevCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5f-112">Puntatore a una struttura [**del \_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) dell'ultimo CRL trovato.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-112">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure of the last CRL found.</span></span> <span data-ttu-id="e4e5f-113">Alla prima chiamata alla funzione, questo parametro deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="e4e5f-114">Nelle chiamate successive deve essere impostato sul puntatore restituito nel parametro *ppProvCRLContext* nell'ultima chiamata.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCRLContext* parameter on the last call.</span></span> <span data-ttu-id="e4e5f-115">Un puntatore non **null** passato in questo parametro viene liberato dalla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="e4e5f-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5f-117">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="e4e5f-118">*ppvStoreProvFindInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5f-119">Puntatore a un puntatore a un buffer per restituire le informazioni sul provider dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="e4e5f-120">Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="e4e5f-121">Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="e4e5f-122">*ppProvCrlContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-122">*ppProvCrlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5f-123">In una ricerca corretta viene restituito un puntatore al CRL trovato in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-123">On a successful find, a pointer to the CRL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e5f-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4e5f-124">Return value</span></span>

<span data-ttu-id="e4e5f-125">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e4e5f-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e5f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4e5f-126">Requirements</span></span>



| <span data-ttu-id="e4e5f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4e5f-127">Requirement</span></span> | <span data-ttu-id="e4e5f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e4e5f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4e5f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4e5f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e5f-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e4e5f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4e5f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e5f-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4e5f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4e5f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4e5f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e5f-134">**\_informazioni su \_ prova \_ archivio \_ certificati**</span><span class="sxs-lookup"><span data-stu-id="e4e5f-134">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="e4e5f-135">**CertFindCRLInStore**</span><span class="sxs-lookup"><span data-stu-id="e4e5f-135">**CertFindCRLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[<span data-ttu-id="e4e5f-136">**\_contesto CRL**</span><span class="sxs-lookup"><span data-stu-id="e4e5f-136">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
