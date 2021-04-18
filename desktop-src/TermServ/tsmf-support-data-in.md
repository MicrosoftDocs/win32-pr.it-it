---
title: Struttura TSMF_SUPPORT_DATA_IN
description: Contiene informazioni sui formati multimediali. | Struttura TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_DATA_IN Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_DATA_IN Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321541"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="0b34f-106">TSMF \_ supporta \_ i dati \_ nella struttura</span><span class="sxs-lookup"><span data-stu-id="0b34f-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="0b34f-107">Contiene informazioni sui formati multimediali.</span><span class="sxs-lookup"><span data-stu-id="0b34f-107">Contains information about media formats.</span></span> <span data-ttu-id="0b34f-108">Questa struttura viene usata dal metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante le query di supporto per il **\_ \_ \_ \_ formato WRDS query MF** .</span><span class="sxs-lookup"><span data-stu-id="0b34f-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b34f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b34f-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="0b34f-110">Members</span><span class="sxs-lookup"><span data-stu-id="0b34f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b34f-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="0b34f-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="0b34f-112">Sessione.</span><span class="sxs-lookup"><span data-stu-id="0b34f-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="0b34f-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="0b34f-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="0b34f-114">Numero di strutture nei dati a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="0b34f-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="0b34f-115">**...**</span><span class="sxs-lookup"><span data-stu-id="0b34f-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="0b34f-116">Numero variabile di strutture che contengono dati di formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="0b34f-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b34f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b34f-117">Requirements</span></span>



| <span data-ttu-id="0b34f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b34f-118">Requirement</span></span> | <span data-ttu-id="0b34f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0b34f-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="0b34f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b34f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0b34f-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0b34f-121">None supported</span></span><br/>         |
| <span data-ttu-id="0b34f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b34f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0b34f-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b34f-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b34f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b34f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b34f-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="0b34f-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="0b34f-126">**\_supporto \_ di TSMF NODEDATA \_ in**</span><span class="sxs-lookup"><span data-stu-id="0b34f-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





