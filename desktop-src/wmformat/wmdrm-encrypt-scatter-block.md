---
title: Struttura WMDRM_ENCRYPT_SCATTER_BLOCK (wmdrmsdk. h)
description: La \_ \_ struttura di blocco a dispersione crittografata WMDRM \_ contiene un blocco di dati da crittografare.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Formato di Windows Media per la struttura WMDRM_ENCRYPT_SCATTER_BLOCK
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324817"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="60b39-105">\_ \_ Struttura blocco a dispersione crittografia WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="60b39-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="60b39-106">La struttura di **\_ \_ \_ blocco a dispersione crittografata WMDRM** contiene un blocco di dati da crittografare.</span><span class="sxs-lookup"><span data-stu-id="60b39-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b39-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60b39-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="60b39-108">Members</span><span class="sxs-lookup"><span data-stu-id="60b39-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="60b39-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="60b39-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="60b39-110">Identificatore del flusso a cui appartiene il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="60b39-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="60b39-111">**cbBlock**</span><span class="sxs-lookup"><span data-stu-id="60b39-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="60b39-112">Dimensioni del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="60b39-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="60b39-113">**pbBlock**</span><span class="sxs-lookup"><span data-stu-id="60b39-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="60b39-114">Puntatore a un buffer contenente il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="60b39-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b39-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="60b39-115">Remarks</span></span>

<span data-ttu-id="60b39-116">Questa struttura viene utilizzata dal metodo [**IWMDRMEncryptScatter:: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) per identificare i blocchi di dati da crittografare.</span><span class="sxs-lookup"><span data-stu-id="60b39-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b39-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60b39-117">Requirements</span></span>



| <span data-ttu-id="60b39-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b39-118">Requirement</span></span> | <span data-ttu-id="60b39-119">Valore</span><span class="sxs-lookup"><span data-stu-id="60b39-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60b39-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60b39-120">Header</span></span><br/> | <dl> <span data-ttu-id="60b39-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b39-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b39-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60b39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b39-123">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="60b39-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





