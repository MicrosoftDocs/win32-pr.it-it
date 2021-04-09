---
description: Chiamato da CertDeleteCTLFromStore prima di eliminare un elenco di scopi consentiti dall'archivio.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Funzione di callback CertStoreProvDeleteCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880997"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="628a0-103">Funzione di callback CertStoreProvDeleteCTL</span><span class="sxs-lookup"><span data-stu-id="628a0-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="628a0-104">La funzione di callback **CertStoreProvDeleteCTL** viene chiamata da [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) prima di eliminare un elenco di scopi consentiti dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="628a0-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="628a0-105">Questa funzione determina se è possibile eliminare un elenco di scopi consentiti.</span><span class="sxs-lookup"><span data-stu-id="628a0-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="628a0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="628a0-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="628a0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="628a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="628a0-108">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="628a0-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628a0-109">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="628a0-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="628a0-110">*pCtlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="628a0-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628a0-111">Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="628a0-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="628a0-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="628a0-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628a0-113">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="628a0-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="628a0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="628a0-114">Return value</span></span>

<span data-ttu-id="628a0-115">Restituisce **true** se è possibile eliminare un CTL dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="628a0-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="628a0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="628a0-116">Requirements</span></span>



| <span data-ttu-id="628a0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="628a0-117">Requirement</span></span> | <span data-ttu-id="628a0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="628a0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="628a0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="628a0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="628a0-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="628a0-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="628a0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="628a0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="628a0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="628a0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
