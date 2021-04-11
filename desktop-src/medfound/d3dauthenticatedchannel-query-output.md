---
description: 'Contiene la risposta del metodo IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127935"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="7726d-103">Struttura di output della \_ query D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="7726d-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="7726d-104">Contiene la risposta del metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="7726d-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7726d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7726d-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="7726d-106">Members</span><span class="sxs-lookup"><span data-stu-id="7726d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7726d-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="7726d-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="7726d-108">Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (Mac) dei dati.</span><span class="sxs-lookup"><span data-stu-id="7726d-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="7726d-109">Il driver utilizza il MAC CBC a chiave singola (OMAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="7726d-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="7726d-110">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="7726d-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="7726d-111">GUID che specifica la query.</span><span class="sxs-lookup"><span data-stu-id="7726d-111">A GUID that specifies the query.</span></span> <span data-ttu-id="7726d-112">Per un elenco di valori, vedere [protezione del contenuto query](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="7726d-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="7726d-113">**GESTIRE**</span><span class="sxs-lookup"><span data-stu-id="7726d-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="7726d-114">Handle per il canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="7726d-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="7726d-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="7726d-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="7726d-116">Numero di sequenza della query.</span><span class="sxs-lookup"><span data-stu-id="7726d-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="7726d-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="7726d-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="7726d-118">Codice risultato per la query.</span><span class="sxs-lookup"><span data-stu-id="7726d-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7726d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7726d-119">Remarks</span></span>

<span data-ttu-id="7726d-120">Per i membri **QueryType**, **hChannel** e **SequenceNumber** , il driver usa gli stessi valori forniti dall'applicazione nella struttura di input della [**\_ query D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md) .</span><span class="sxs-lookup"><span data-stu-id="7726d-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="7726d-121">L'applicazione deve verificare che questi valori corrispondano.</span><span class="sxs-lookup"><span data-stu-id="7726d-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="7726d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7726d-122">Requirements</span></span>



| <span data-ttu-id="7726d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7726d-123">Requirement</span></span> | <span data-ttu-id="7726d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7726d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7726d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7726d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7726d-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7726d-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7726d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7726d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7726d-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7726d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7726d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7726d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7726d-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7726d-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7726d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7726d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7726d-132">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="7726d-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="7726d-133">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="7726d-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




