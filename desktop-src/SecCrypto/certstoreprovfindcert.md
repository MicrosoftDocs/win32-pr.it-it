---
description: Enumera o trova il primo o il certificato successivo in un archivio esterno che corrisponde ai criteri specificati.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Funzione di callback CertStoreProvFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347076"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="d93e7-103">Funzione di callback CertStoreProvFindCert</span><span class="sxs-lookup"><span data-stu-id="d93e7-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="d93e7-104">La funzione di callback **CertStoreProvFindCert** enumera o trova il primo o il certificato successivo in un [*archivio esterno*](../secgloss/e-gly.md) che corrisponde ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="d93e7-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d93e7-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="d93e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d93e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93e7-107">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e7-108">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d93e7-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d93e7-109">*pFindInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e7-110">Un puntatore a un [**\_ archivio certificati \_ prova a \_ trovare \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la struttura di informazioni contenente tutti i parametri passati alla funzione [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .</span><span class="sxs-lookup"><span data-stu-id="d93e7-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="d93e7-111">*pPrevCertContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e7-112">Puntatore a un [**\_ contesto CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato trovato.</span><span class="sxs-lookup"><span data-stu-id="d93e7-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="d93e7-113">Alla prima chiamata alla funzione, questo parametro deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="d93e7-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="d93e7-114">Nelle chiamate successive deve essere impostato sul puntatore restituito nel parametro *ppProvCertContext* nell'ultima chiamata.</span><span class="sxs-lookup"><span data-stu-id="d93e7-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="d93e7-115">Un puntatore non **null** passato in questo parametro viene liberato dalla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="d93e7-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d93e7-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e7-117">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="d93e7-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="d93e7-118">*ppvStoreProvFindInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e7-119">Puntatore a un puntatore a un buffer per restituire le informazioni sul provider dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="d93e7-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="d93e7-120">Facoltativamente, il callback può restituire un puntatore alle informazioni di ricerca interne in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d93e7-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="d93e7-121">Dopo la prima chiamata, questo parametro viene impostato sul puntatore restituito dalla chiamata precedente alla funzione.</span><span class="sxs-lookup"><span data-stu-id="d93e7-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="d93e7-122">*ppProvCertContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e7-123">In una ricerca corretta viene restituito un puntatore al certificato trovato in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d93e7-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d93e7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d93e7-124">Return value</span></span>

<span data-ttu-id="d93e7-125">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d93e7-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="d93e7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d93e7-126">Requirements</span></span>



| <span data-ttu-id="d93e7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d93e7-127">Requirement</span></span> | <span data-ttu-id="d93e7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d93e7-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d93e7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d93e7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d93e7-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d93e7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d93e7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d93e7-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d93e7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d93e7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d93e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93e7-134">**contesto del certificato \_**</span><span class="sxs-lookup"><span data-stu-id="d93e7-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="d93e7-135">**\_informazioni su \_ prova \_ archivio \_ certificati**</span><span class="sxs-lookup"><span data-stu-id="d93e7-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="d93e7-136">**CertFindCertificateInStore**</span><span class="sxs-lookup"><span data-stu-id="d93e7-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
