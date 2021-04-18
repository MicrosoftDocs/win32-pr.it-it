---
description: Chiamato quando il certificato restituito dal callback CertStoreProvFindCTL non è stato usato e quindi rilasciato, in una chiamata successiva a CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Funzione di callback CertStoreProvFreeFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310944"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="42209-103">Funzione di callback CertStoreProvFreeFindCTL</span><span class="sxs-lookup"><span data-stu-id="42209-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="42209-104">La funzione di callback **CertStoreProvFreeFindCTL** viene chiamata quando il certificato restituito dal callback [**CertStoreProvFindCTL**](certstoreprovfindctl.md) non è stato usato e quindi rilasciato in una chiamata successiva a **CertStoreProvFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="42209-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="42209-105">Prima che venga chiamato il callback di chiusura, tutti i certificati restituiti dal callback [**CertStoreProvFindCTL**](certstoreprovfindctl.md) devono essere rilasciati dal provider utilizzando **CertStoreProvFindCTL** o **CertStoreProvFreeFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="42209-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="42209-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42209-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="42209-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="42209-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42209-108">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42209-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42209-109">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="42209-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="42209-110">*pCtlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42209-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42209-111">Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="42209-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="42209-112">*pvStoreProvFindInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42209-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42209-113">Puntatore a un buffer contenente le informazioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="42209-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="42209-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42209-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42209-115">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="42209-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42209-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42209-116">Return value</span></span>

<span data-ttu-id="42209-117">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="42209-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="42209-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42209-118">Requirements</span></span>



| <span data-ttu-id="42209-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="42209-119">Requirement</span></span> | <span data-ttu-id="42209-120">Valore</span><span class="sxs-lookup"><span data-stu-id="42209-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42209-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42209-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42209-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42209-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="42209-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42209-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42209-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42209-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42209-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42209-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42209-126">**CertStoreProvFindCTL**</span><span class="sxs-lookup"><span data-stu-id="42209-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="42209-127">**\_contesto CTL**</span><span class="sxs-lookup"><span data-stu-id="42209-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
