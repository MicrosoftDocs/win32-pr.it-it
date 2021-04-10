---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCRL non è stato usato e quindi rilasciato, in una chiamata successiva a CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Funzione di callback CertStoreProvFreeFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883813"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="2ce9a-103">Funzione di callback CertStoreProvFreeFindCRL</span><span class="sxs-lookup"><span data-stu-id="2ce9a-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="2ce9a-104">La funzione di callback **CertStoreProvFreeFindCRL** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="2ce9a-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="2ce9a-105">Prima che venga chiamato il callback di chiusura, tutti i certificati restituiti dal callback [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) devono essere rilasciati dal provider utilizzando **CertStoreProvFindCRL** o **CertStoreProvFreeFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="2ce9a-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce9a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ce9a-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2ce9a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ce9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce9a-108">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ce9a-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce9a-109">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2ce9a-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ce9a-110">*pCrlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ce9a-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce9a-111">Puntatore a un [**\_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="2ce9a-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="2ce9a-112">*pvStoreProvFindInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ce9a-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce9a-113">Puntatore a un buffer contenente le informazioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2ce9a-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="2ce9a-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ce9a-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce9a-115">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="2ce9a-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce9a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ce9a-116">Return value</span></span>

<span data-ttu-id="2ce9a-117">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2ce9a-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce9a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ce9a-118">Requirements</span></span>



| <span data-ttu-id="2ce9a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ce9a-119">Requirement</span></span> | <span data-ttu-id="2ce9a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2ce9a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ce9a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ce9a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce9a-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2ce9a-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2ce9a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ce9a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce9a-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ce9a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ce9a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ce9a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce9a-126">**CertStoreProvFindCRL**</span><span class="sxs-lookup"><span data-stu-id="2ce9a-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="2ce9a-127">**\_contesto CRL**</span><span class="sxs-lookup"><span data-stu-id="2ce9a-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
