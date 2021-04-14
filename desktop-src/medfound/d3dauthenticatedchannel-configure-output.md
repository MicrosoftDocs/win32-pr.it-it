---
description: 'Contiene la risposta a una chiamata al metodo IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342536"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a><span data-ttu-id="4d75c-103">D3DAUTHENTICATEDCHANNEL \_ configurare la \_ struttura di output</span><span class="sxs-lookup"><span data-stu-id="4d75c-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_OUTPUT structure</span></span>

<span data-ttu-id="4d75c-104">Contiene la risposta a una chiamata al metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="4d75c-104">Contains the response to a call to the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d75c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d75c-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="4d75c-106">Members</span><span class="sxs-lookup"><span data-stu-id="4d75c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d75c-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="4d75c-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="4d75c-108">Struttura [**\_ OMAC D3D**](d3d-omac.md) che contiene un Message Authentication Code (Mac) dei dati.</span><span class="sxs-lookup"><span data-stu-id="4d75c-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="4d75c-109">Il driver utilizza il MAC CBC a chiave singola (OMAC) basato su AES per calcolare questo valore per il blocco di dati visualizzato dopo questo membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="4d75c-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="4d75c-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="4d75c-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="4d75c-111">GUID che specifica il comando.</span><span class="sxs-lookup"><span data-stu-id="4d75c-111">A GUID that specifies the command.</span></span> <span data-ttu-id="4d75c-112">Per un elenco di valori, vedere [protezione del contenuto comandi](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="4d75c-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d75c-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="4d75c-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="4d75c-114">Handle per il canale autenticato.</span><span class="sxs-lookup"><span data-stu-id="4d75c-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="4d75c-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="4d75c-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="4d75c-116">Numero di sequenza del comando.</span><span class="sxs-lookup"><span data-stu-id="4d75c-116">The command sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="4d75c-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="4d75c-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="4d75c-118">Codice risultato per il comando.</span><span class="sxs-lookup"><span data-stu-id="4d75c-118">The result code for the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d75c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d75c-119">Remarks</span></span>

<span data-ttu-id="4d75c-120">Per i membri **ConfigureType**, **hChannel** e **SequenceNumber** , il driver usa gli stessi valori forniti dall'applicazione in D3DAUTHENTICATEDCHANNEL configurare la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) .</span><span class="sxs-lookup"><span data-stu-id="4d75c-120">For the **ConfigureType**, **hChannel**, and **SequenceNumber** members, the driver uses the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure.</span></span> <span data-ttu-id="4d75c-121">L'applicazione deve verificare che questi valori corrispondano.</span><span class="sxs-lookup"><span data-stu-id="4d75c-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d75c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d75c-122">Requirements</span></span>



| <span data-ttu-id="4d75c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d75c-123">Requirement</span></span> | <span data-ttu-id="4d75c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4d75c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d75c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d75c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4d75c-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4d75c-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4d75c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d75c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4d75c-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d75c-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4d75c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d75c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d75c-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d75c-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d75c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d75c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d75c-132">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="4d75c-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4d75c-133">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="4d75c-133">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




