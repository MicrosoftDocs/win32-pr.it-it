---
description: Contiene i dati di input per un \_ comando D3DAUTHENTICATEDCONFIGURE Initialize.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049315"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="dd3d8-103">\_Struttura D3DAUTHENTICATEDCHANNEL CONFIGUREINITIALIZE</span><span class="sxs-lookup"><span data-stu-id="dd3d8-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="dd3d8-104">Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="dd3d8-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="dd3d8-105">Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="dd3d8-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd3d8-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="dd3d8-107">Members</span><span class="sxs-lookup"><span data-stu-id="dd3d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd3d8-108">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="dd3d8-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="dd3d8-109">D3DAUTHENTICATEDCHANNEL configura la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.</span><span class="sxs-lookup"><span data-stu-id="dd3d8-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="dd3d8-110">**StartSequenceQuery**</span><span class="sxs-lookup"><span data-stu-id="dd3d8-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="dd3d8-111">Numero di sequenza iniziale per le query.</span><span class="sxs-lookup"><span data-stu-id="dd3d8-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="dd3d8-112">**StartSequenceConfigure**</span><span class="sxs-lookup"><span data-stu-id="dd3d8-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="dd3d8-113">Numero di sequenza iniziale per i comandi.</span><span class="sxs-lookup"><span data-stu-id="dd3d8-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd3d8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd3d8-114">Remarks</span></span>

<span data-ttu-id="dd3d8-115">I membri **StartSequenceQuery** e **StartSequenceConfigure** contengono ognuno un numero casuale a 32 bit a crittografia sicura.</span><span class="sxs-lookup"><span data-stu-id="dd3d8-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3d8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd3d8-116">Requirements</span></span>



| <span data-ttu-id="dd3d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd3d8-117">Requirement</span></span> | <span data-ttu-id="dd3d8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dd3d8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3d8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd3d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3d8-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dd3d8-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd3d8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd3d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3d8-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3d8-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dd3d8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd3d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3d8-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3d8-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd3d8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd3d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3d8-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="dd3d8-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="dd3d8-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="dd3d8-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




