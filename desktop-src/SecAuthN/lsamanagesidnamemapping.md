---
UID: ''
title: LsaManageSidNameMapping (funzione)
description: Aggiunge o rimuove i mapping SID/nome dal set di mapping registrato con il servizio di ricerca LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "104336618"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="66c42-103">LsaManageSidNameMapping (funzione)</span><span class="sxs-lookup"><span data-stu-id="66c42-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="66c42-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66c42-104">Description</span></span>

<span data-ttu-id="66c42-105">La funzione **LsaManageSidNameMapping** aggiunge o rimuove i mapping SID/Name dal set di mapping registrato con il servizio di ricerca LSA.</span><span class="sxs-lookup"><span data-stu-id="66c42-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="66c42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66c42-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="66c42-107">OpType [in]</span><span class="sxs-lookup"><span data-stu-id="66c42-107">OpType [in]</span></span>

<span data-ttu-id="66c42-108">Indica se è in corso la chiamata di questa funzione per aggiungere o rimuovere un mapping SID/Name.</span><span class="sxs-lookup"><span data-stu-id="66c42-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="66c42-109">OpInput [in]</span><span class="sxs-lookup"><span data-stu-id="66c42-109">OpInput [in]</span></span>

<span data-ttu-id="66c42-110">Indica i valori di dominio, account e SID da utilizzare durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="66c42-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="66c42-111">È anche possibile impostare flag aggiuntivi all'interno di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="66c42-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="66c42-112">OpOutput [out]</span><span class="sxs-lookup"><span data-stu-id="66c42-112">OpOutput [out]</span></span>

<span data-ttu-id="66c42-113">Contiene un valore di [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) che indica l'esito positivo o negativo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="66c42-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="66c42-114">Valore</span><span class="sxs-lookup"><span data-stu-id="66c42-114">Value</span></span> | <span data-ttu-id="66c42-115">Significato</span><span class="sxs-lookup"><span data-stu-id="66c42-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="66c42-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="66c42-116">**Success**</span></span> | <span data-ttu-id="66c42-117">L'operazione è stata completata senza errori.</span><span class="sxs-lookup"><span data-stu-id="66c42-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="66c42-118">**NonMappingError**</span><span class="sxs-lookup"><span data-stu-id="66c42-118">**NonMappingError**</span></span> | <span data-ttu-id="66c42-119">Si è verificato un errore non correlato al mapping del nome SID.</span><span class="sxs-lookup"><span data-stu-id="66c42-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="66c42-120">**NameCollision**</span><span class="sxs-lookup"><span data-stu-id="66c42-120">**NameCollision**</span></span> | <span data-ttu-id="66c42-121">Operazione non riuscita a causa di un conflitto di nomi.</span><span class="sxs-lookup"><span data-stu-id="66c42-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="66c42-122">**SidCollision**</span><span class="sxs-lookup"><span data-stu-id="66c42-122">**SidCollision**</span></span> | <span data-ttu-id="66c42-123">Operazione non riuscita a causa di un conflitto SID.</span><span class="sxs-lookup"><span data-stu-id="66c42-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="66c42-124">**DomainNotFound**</span><span class="sxs-lookup"><span data-stu-id="66c42-124">**DomainNotFound**</span></span> | <span data-ttu-id="66c42-125">Dominio corrispondente non trovato.</span><span class="sxs-lookup"><span data-stu-id="66c42-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="66c42-126">**DomainSidPrefixMismatch**</span><span class="sxs-lookup"><span data-stu-id="66c42-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="66c42-127">Il prefisso di dominio del SID specificato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="66c42-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="66c42-128">**MappingNotFound**</span><span class="sxs-lookup"><span data-stu-id="66c42-128">**MappingNotFound**</span></span> | <span data-ttu-id="66c42-129">Il mapping non è stato trovato nella cache.</span><span class="sxs-lookup"><span data-stu-id="66c42-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="66c42-130">Restituisce</span><span class="sxs-lookup"><span data-stu-id="66c42-130">Returns</span></span>

<span data-ttu-id="66c42-131">Se il mapping viene inserito correttamente, il valore restituito viene STATUS_SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="66c42-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="66c42-132">In caso contrario, se la funzione ha esito negativo a causa di conflitti di nome o SID, viene restituito STATUS_INVALID_PARAMETER errore.</span><span class="sxs-lookup"><span data-stu-id="66c42-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c42-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="66c42-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="66c42-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="66c42-134">See also</span></span>
