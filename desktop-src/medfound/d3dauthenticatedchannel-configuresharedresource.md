---
description: Contiene i dati di input per un \_ comando D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305452"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="893c2-103">\_Struttura D3DAUTHENTICATEDCHANNEL CONFIGURESHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="893c2-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="893c2-104">Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="893c2-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="893c2-105">Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="893c2-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="893c2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="893c2-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="893c2-107">Members</span><span class="sxs-lookup"><span data-stu-id="893c2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="893c2-108">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="893c2-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="893c2-109">D3DAUTHENTICATEDCHANNEL configura la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.</span><span class="sxs-lookup"><span data-stu-id="893c2-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="893c2-110">**ProcessIdentiferType**</span><span class="sxs-lookup"><span data-stu-id="893c2-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="893c2-111">Valore [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) che specifica il tipo di processo.</span><span class="sxs-lookup"><span data-stu-id="893c2-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="893c2-112">Per specificare il processo di Gestione finestre desktop (DWM), impostare questo membro su **PROCESSIDTYPE \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="893c2-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="893c2-113">In caso contrario, impostare questo membro su **PROCESSIDTYPE \_ handle** e impostare il membro **ProcessHandle** su un handle valido.</span><span class="sxs-lookup"><span data-stu-id="893c2-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="893c2-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="893c2-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="893c2-115">Handle di processo.</span><span class="sxs-lookup"><span data-stu-id="893c2-115">A process handle.</span></span> <span data-ttu-id="893c2-116">Se il membro **ProcessIdentifier** è uguale **all' \_ handle PROCESSTIDTYPE**, il membro **ProcessHandle** specifica un handle per un processo.</span><span class="sxs-lookup"><span data-stu-id="893c2-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="893c2-117">In caso contrario, il valore viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="893c2-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="893c2-118">**AllowAccess**</span><span class="sxs-lookup"><span data-stu-id="893c2-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="893c2-119">Se **true**, il processo specificato ha accesso alle risorse condivise limitate.</span><span class="sxs-lookup"><span data-stu-id="893c2-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="893c2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="893c2-120">Requirements</span></span>



| <span data-ttu-id="893c2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="893c2-121">Requirement</span></span> | <span data-ttu-id="893c2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="893c2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="893c2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="893c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="893c2-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="893c2-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="893c2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="893c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="893c2-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="893c2-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="893c2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="893c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="893c2-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="893c2-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="893c2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="893c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893c2-130">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="893c2-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="893c2-131">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="893c2-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




