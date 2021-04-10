---
description: 'Contiene i dati di input per il metodo IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Struttura D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225820"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a><span data-ttu-id="f5105-103">Struttura di input della \_ query D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="f5105-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT structure</span></span>

<span data-ttu-id="f5105-104">Contiene i dati di input per il metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="f5105-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5105-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5105-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a><span data-ttu-id="f5105-106">Members</span><span class="sxs-lookup"><span data-stu-id="f5105-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5105-107">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="f5105-107">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="f5105-108">GUID che specifica la query.</span><span class="sxs-lookup"><span data-stu-id="f5105-108">A GUID that specifies the query.</span></span> <span data-ttu-id="f5105-109">Per un elenco di valori, vedere [protezione del contenuto query](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="f5105-109">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5105-110">**GESTIRE**</span><span class="sxs-lookup"><span data-stu-id="f5105-110">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="f5105-111">Handle per il canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="f5105-111">A handle to the authenticated channel.</span></span> <span data-ttu-id="f5105-112">Per ottenere l'handle, chiamare [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="f5105-112">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="f5105-113">**UINT**</span><span class="sxs-lookup"><span data-stu-id="f5105-113">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="f5105-114">Numero di sequenza della query.</span><span class="sxs-lookup"><span data-stu-id="f5105-114">The query sequence number.</span></span> <span data-ttu-id="f5105-115">All'inizio della sessione, generare un numero casuale a 32 bit a crittografia sicura da usare come numero di sequenza iniziale.</span><span class="sxs-lookup"><span data-stu-id="f5105-115">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="f5105-116">Per ogni query, incrementare il numero di sequenza di 1.</span><span class="sxs-lookup"><span data-stu-id="f5105-116">For each query, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5105-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5105-117">Requirements</span></span>



| <span data-ttu-id="f5105-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5105-118">Requirement</span></span> | <span data-ttu-id="f5105-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f5105-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5105-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5105-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5105-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5105-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5105-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5105-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5105-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5105-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f5105-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5105-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5105-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5105-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5105-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5105-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5105-127">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="f5105-127">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f5105-128">**IDirect3DAuthenticatedChannel9:: query**</span><span class="sxs-lookup"><span data-stu-id="f5105-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




