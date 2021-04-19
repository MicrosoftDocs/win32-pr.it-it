---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCert non è stato usato e quindi rilasciato, in una chiamata successiva a CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Funzione di callback CertStoreProvFreeFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315805"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="0e9a6-103">Funzione di callback CertStoreProvFreeFindCert</span><span class="sxs-lookup"><span data-stu-id="0e9a6-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="0e9a6-104">La funzione di callback **CertStoreProvFreeFindCert** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCert**](certstoreprovfindcert.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCert**.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="0e9a6-105">Prima che venga chiamato il callback di chiusura, tutti i certificati restituiti dal callback [**CertStoreProvFindCert**](certstoreprovfindcert.md) devono essere rilasciati dal provider utilizzando **CertStoreProvFindCert** o **CertStoreProvFreeFindCert**.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9a6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e9a6-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0e9a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e9a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9a6-108">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9a6-109">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0e9a6-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e9a6-110">*pCertContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9a6-111">Puntatore a un [**\_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="0e9a6-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="0e9a6-112">*pvStoreProvFindInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9a6-113">Puntatore a un buffer contenente le informazioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="0e9a6-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9a6-115">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9a6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e9a6-116">Return value</span></span>

<span data-ttu-id="0e9a6-117">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0e9a6-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9a6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e9a6-118">Requirements</span></span>



| <span data-ttu-id="0e9a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e9a6-119">Requirement</span></span> | <span data-ttu-id="0e9a6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0e9a6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e9a6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e9a6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9a6-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0e9a6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e9a6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9a6-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e9a6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e9a6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e9a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9a6-126">**contesto del certificato \_**</span><span class="sxs-lookup"><span data-stu-id="0e9a6-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="0e9a6-127">**CertStoreProvFindCert**</span><span class="sxs-lookup"><span data-stu-id="0e9a6-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
