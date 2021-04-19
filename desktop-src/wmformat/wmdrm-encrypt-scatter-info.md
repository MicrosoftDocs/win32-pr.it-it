---
title: Struttura WMDRM_ENCRYPT_SCATTER_INFO (wmdrmsdk. h)
description: La \_ struttura di \_ informazioni per la crittografia a dispersione WMDRM \_ contiene le informazioni necessarie per configurare l'interfaccia IWMDRMEncryptScatter per l'uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Formato di Windows Media per la struttura WMDRM_ENCRYPT_SCATTER_INFO
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326606"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="7c878-105">\_Struttura delle \_ informazioni di dispersione di crittografia WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="7c878-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="7c878-106">La struttura di informazioni per la **\_ crittografia a \_ dispersione \_ WMDRM** contiene le informazioni necessarie per configurare l'interfaccia [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) per l'uso.</span><span class="sxs-lookup"><span data-stu-id="7c878-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c878-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c878-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="7c878-108">Members</span><span class="sxs-lookup"><span data-stu-id="7c878-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c878-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="7c878-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="7c878-110">Identificatore del flusso da crittografare.</span><span class="sxs-lookup"><span data-stu-id="7c878-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="7c878-111">**dwSampleProtectionVersion**</span><span class="sxs-lookup"><span data-stu-id="7c878-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7c878-112">Versione di esempio di protezione da usare per codificare i dati dal flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="7c878-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="7c878-113">**cbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="7c878-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7c878-114">Dimensioni del buffer **pbProtectionInfo** in byte.</span><span class="sxs-lookup"><span data-stu-id="7c878-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7c878-115">**pbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="7c878-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7c878-116">Buffer contenente informazioni aggiuntive sulla protezione.</span><span class="sxs-lookup"><span data-stu-id="7c878-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c878-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c878-117">Remarks</span></span>

<span data-ttu-id="7c878-118">Questa struttura viene utilizzata dal metodo [**IWMDRMEncryptScatter:: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) .</span><span class="sxs-lookup"><span data-stu-id="7c878-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c878-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c878-119">Requirements</span></span>



| <span data-ttu-id="7c878-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c878-120">Requirement</span></span> | <span data-ttu-id="7c878-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7c878-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c878-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c878-122">Header</span></span><br/> | <dl> <span data-ttu-id="7c878-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c878-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c878-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c878-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c878-125">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="7c878-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





