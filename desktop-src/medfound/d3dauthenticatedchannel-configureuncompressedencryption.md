---
description: Contiene i dati di input per il \_ comando D3DAUTHENTICATEDCONFIGURE ENCRYPTIONWHENACCESSIBLE.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: Struttura D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305451"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="733c0-103">\_Struttura D3DAUTHENTICATEDCHANNEL CONFIGUREUNCOMPRESSEDENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="733c0-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="733c0-104">Contiene i dati di input per il comando [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .</span><span class="sxs-lookup"><span data-stu-id="733c0-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="733c0-105">Per inviare questa query, chiamare [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="733c0-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="733c0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="733c0-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="733c0-107">Members</span><span class="sxs-lookup"><span data-stu-id="733c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="733c0-108">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="733c0-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="733c0-109">D3DAUTHENTICATEDCHANNEL configura la struttura di [**\_ \_ input**](d3dauthenticatedchannel-configure-input.md) che contiene il GUID del comando e altri dati.</span><span class="sxs-lookup"><span data-stu-id="733c0-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="733c0-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="733c0-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="733c0-111">GUID che specifica il tipo di crittografia da applicare.</span><span class="sxs-lookup"><span data-stu-id="733c0-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="733c0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="733c0-112">Requirements</span></span>



| <span data-ttu-id="733c0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="733c0-113">Requirement</span></span> | <span data-ttu-id="733c0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="733c0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="733c0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="733c0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="733c0-116">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="733c0-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="733c0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="733c0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="733c0-118">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="733c0-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="733c0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="733c0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="733c0-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="733c0-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733c0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="733c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733c0-122">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="733c0-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="733c0-123">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="733c0-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




