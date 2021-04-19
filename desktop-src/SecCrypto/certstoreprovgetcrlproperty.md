---
description: Recupera una proprietà specificata di un CRL.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Funzione di callback CertStoreProvGetCRLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310942"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="dccf2-103">Funzione di callback CertStoreProvGetCRLProperty</span><span class="sxs-lookup"><span data-stu-id="dccf2-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="dccf2-104">La funzione di callback **CertStoreProvGetCRLProperty** recupera una proprietà specificata di un [*CRL*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dccf2-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dccf2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dccf2-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="dccf2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dccf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccf2-107">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccf2-108">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dccf2-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccf2-109">*pCrlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccf2-110">Puntatore a una struttura [**del \_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .</span><span class="sxs-lookup"><span data-stu-id="dccf2-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dccf2-111">*dwPropId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccf2-112">Indica un identificatore di proprietà.</span><span class="sxs-lookup"><span data-stu-id="dccf2-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dccf2-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccf2-114">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="dccf2-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="dccf2-115">*pvData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dccf2-116">Puntatore a un buffer che contiene il puntatore a una struttura [**del \_ contesto CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) che deve essere restituita dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="dccf2-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="dccf2-117">Può essere impostato su **null** in una prima chiamata alla funzione per ottenere il valore di *pcbData* prima di allocare memoria per il buffer.</span><span class="sxs-lookup"><span data-stu-id="dccf2-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dccf2-118">*pcbData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dccf2-119">Puntatore a un **valore DWORD** che indica la lunghezza del buffer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="dccf2-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccf2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dccf2-120">Return value</span></span>

<span data-ttu-id="dccf2-121">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="dccf2-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="dccf2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dccf2-122">Requirements</span></span>



| <span data-ttu-id="dccf2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dccf2-123">Requirement</span></span> | <span data-ttu-id="dccf2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dccf2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dccf2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dccf2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dccf2-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="dccf2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dccf2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dccf2-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dccf2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dccf2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dccf2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccf2-130">**\_contesto CRL**</span><span class="sxs-lookup"><span data-stu-id="dccf2-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
