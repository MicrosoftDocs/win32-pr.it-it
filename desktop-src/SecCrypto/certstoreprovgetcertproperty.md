---
description: Recupera una proprietà specificata di un certificato.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Funzione di callback CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310943"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="e1526-103">Funzione di callback CertStoreProvGetCertProperty</span><span class="sxs-lookup"><span data-stu-id="e1526-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="e1526-104">La funzione di callback **CertStoreProvGetCertProperty** recupera una proprietà specificata di un certificato.</span><span class="sxs-lookup"><span data-stu-id="e1526-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1526-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1526-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="e1526-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1526-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1526-107">*hStoreProv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1526-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1526-108">Handle **HCERTSTOREPROV** per un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e1526-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1526-109">*pCertContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1526-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1526-110">Puntatore a una struttura [**del \_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="e1526-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e1526-111">*dwPropId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1526-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1526-112">Indica un identificatore di proprietà.</span><span class="sxs-lookup"><span data-stu-id="e1526-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e1526-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1526-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1526-114">Tutti i valori di flag necessari.</span><span class="sxs-lookup"><span data-stu-id="e1526-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="e1526-115">*pvData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e1526-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1526-116">Puntatore a un buffer che contiene il puntatore a una struttura [**del \_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) che deve essere restituita dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="e1526-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="e1526-117">Può essere impostato su **null** in una prima chiamata alla funzione per ottenere il valore di *pcbData* prima di allocare memoria per il buffer.</span><span class="sxs-lookup"><span data-stu-id="e1526-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e1526-118">*pcbData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e1526-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1526-119">Puntatore a un **valore DWORD** che indica la lunghezza del buffer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="e1526-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1526-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1526-120">Return value</span></span>

<span data-ttu-id="e1526-121">Restituisce **true** se la funzione ha esito positivo o **false** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e1526-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1526-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1526-122">Requirements</span></span>



| <span data-ttu-id="e1526-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1526-123">Requirement</span></span> | <span data-ttu-id="e1526-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e1526-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1526-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1526-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e1526-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1526-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e1526-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1526-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e1526-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1526-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1526-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1526-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1526-130">**contesto del certificato \_**</span><span class="sxs-lookup"><span data-stu-id="e1526-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
