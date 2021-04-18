---
description: Recupera una proprietà specificata di un elenco di certificati attendibili (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Funzione di callback CertStoreProvGetCTLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315804"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="318be-103">Funzione di callback CertStoreProvGetCTLProperty</span><span class="sxs-lookup"><span data-stu-id="318be-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="318be-104">La funzione di callback **CertStoreProvGetCTLProperty** recupera una proprietà specificata di un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="318be-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="318be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="318be-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="318be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="318be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="318be-107">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318be-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318be-108">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="318be-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="318be-109">*pCtlContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318be-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318be-110">Puntatore a una struttura [**di \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="318be-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="318be-111">*dwPropId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318be-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318be-112">Indica un identificatore di proprietà.</span><span class="sxs-lookup"><span data-stu-id="318be-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="318be-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="318be-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="318be-114">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="318be-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="318be-115">*pvData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="318be-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="318be-116">Puntatore a un buffer che contiene il puntatore a una struttura [**del \_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) che deve essere restituita dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="318be-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="318be-117">Per ottenere il valore di *pcbData* prima di allocare memoria per il buffer, questo parametro può essere impostato su **null** in una prima chiamata alla funzione.</span><span class="sxs-lookup"><span data-stu-id="318be-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="318be-118">*pcbData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="318be-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="318be-119">Puntatore a un **valore DWORD** che indica la lunghezza del buffer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="318be-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="318be-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="318be-120">Return value</span></span>

<span data-ttu-id="318be-121">Se la funzione ha esito positivo, la funzione restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="318be-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="318be-122">Se la funzione ha esito negativo, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="318be-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="318be-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="318be-123">Requirements</span></span>



| <span data-ttu-id="318be-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="318be-124">Requirement</span></span> | <span data-ttu-id="318be-125">Valore</span><span class="sxs-lookup"><span data-stu-id="318be-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="318be-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="318be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="318be-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="318be-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="318be-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="318be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="318be-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="318be-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="318be-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="318be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318be-131">**\_contesto CTL**</span><span class="sxs-lookup"><span data-stu-id="318be-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
