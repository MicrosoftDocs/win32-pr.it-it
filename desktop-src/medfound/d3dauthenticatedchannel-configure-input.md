---
description: 'Contiene i dati di input per il metodo IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225822"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="a6127-103">D3DAUTHENTICATEDCHANNEL \_ configurare la \_ struttura di input</span><span class="sxs-lookup"><span data-stu-id="a6127-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="a6127-104">Contiene i dati di input per il metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="a6127-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6127-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6127-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="a6127-106">Members</span><span class="sxs-lookup"><span data-stu-id="a6127-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6127-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="a6127-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="a6127-108">Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (Mac) dei dati.</span><span class="sxs-lookup"><span data-stu-id="a6127-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="a6127-109">Il driver utilizza il MAC CBC a chiave singola (OMAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="a6127-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="a6127-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="a6127-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="a6127-111">GUID che specifica il comando.</span><span class="sxs-lookup"><span data-stu-id="a6127-111">A GUID that specifies the command.</span></span> <span data-ttu-id="a6127-112">Per un elenco di valori, vedere [protezione del contenuto comandi](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="a6127-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6127-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="a6127-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="a6127-114">Handle per il canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="a6127-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="a6127-115">Per ottenere l'handle, chiamare [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="a6127-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="a6127-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="a6127-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a6127-117">Numero di sequenza della query.</span><span class="sxs-lookup"><span data-stu-id="a6127-117">The query sequence number.</span></span> <span data-ttu-id="a6127-118">All'inizio della sessione, generare un numero casuale a 32 bit a crittografia sicura da usare come numero di sequenza iniziale.</span><span class="sxs-lookup"><span data-stu-id="a6127-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="a6127-119">Per ogni comando, incrementare il numero di sequenza di 1.</span><span class="sxs-lookup"><span data-stu-id="a6127-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6127-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6127-120">Requirements</span></span>



| <span data-ttu-id="a6127-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6127-121">Requirement</span></span> | <span data-ttu-id="a6127-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a6127-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6127-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6127-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a6127-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a6127-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a6127-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6127-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a6127-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6127-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a6127-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6127-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6127-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6127-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6127-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6127-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6127-130">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="a6127-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a6127-131">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="a6127-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




