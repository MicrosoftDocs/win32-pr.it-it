---
title: Struttura TSMF_SUPPORT_DATA_OUT
description: Contiene informazioni sui formati multimediali. | Struttura TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_DATA_OUT Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_DATA_OUT Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969074"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="20686-106">TSMF \_ supporta la \_ struttura dei dati in \_ uscita</span><span class="sxs-lookup"><span data-stu-id="20686-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="20686-107">Contiene informazioni sui formati multimediali.</span><span class="sxs-lookup"><span data-stu-id="20686-107">Contains information about media formats.</span></span> <span data-ttu-id="20686-108">Questa struttura viene usata dal metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante le query di supporto per il **\_ \_ \_ \_ formato WRDS query MF** .</span><span class="sxs-lookup"><span data-stu-id="20686-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="20686-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20686-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="20686-110">Members</span><span class="sxs-lookup"><span data-stu-id="20686-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="20686-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="20686-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="20686-112">Deve corrispondere alla proprietà **guidMfSession** nei [**\_ \_ dati \_ di supporto TSMF corrispondenti nella**](tsmf-support-data-in.md) struttura.</span><span class="sxs-lookup"><span data-stu-id="20686-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="20686-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="20686-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="20686-114">Numero di strutture nei dati a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="20686-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="20686-115">**...**</span><span class="sxs-lookup"><span data-stu-id="20686-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="20686-116">Numero variabile di strutture che contengono dati di formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="20686-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20686-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20686-117">Requirements</span></span>



| <span data-ttu-id="20686-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="20686-118">Requirement</span></span> | <span data-ttu-id="20686-119">Valore</span><span class="sxs-lookup"><span data-stu-id="20686-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="20686-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20686-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20686-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="20686-121">None supported</span></span><br/>         |
| <span data-ttu-id="20686-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20686-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20686-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="20686-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20686-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20686-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20686-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="20686-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="20686-126">**\_NODEDATA di supporto TSMF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20686-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





