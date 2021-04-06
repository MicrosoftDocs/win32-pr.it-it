---
title: Struttura PROTOCOL_SPECIFIC_DATA (RTM. h)
description: La \_ \_ struttura dei dati specifica del protocollo contiene memoria riservata per i dati specifici di un determinato protocollo di routing.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- RAS struttura PROTOCOL_SPECIFIC_DATA
- RAS puntatore alla struttura PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742191"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="9475e-105">\_ \_ Struttura dei dati specifici del protocollo</span><span class="sxs-lookup"><span data-stu-id="9475e-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="9475e-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9475e-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9475e-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="9475e-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9475e-108">La **struttura \_ \_ dei dati specifica del protocollo** contiene memoria riservata per i dati specifici di un determinato protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="9475e-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="9475e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9475e-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="9475e-110">Members</span><span class="sxs-lookup"><span data-stu-id="9475e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9475e-111">**\_Dati PSD**</span><span class="sxs-lookup"><span data-stu-id="9475e-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="9475e-112">Specifica una matrice di variabili **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9475e-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="9475e-113">Questa memoria è riservata ai dati specifici dei protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="9475e-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9475e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9475e-114">Requirements</span></span>



| <span data-ttu-id="9475e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9475e-115">Requirement</span></span> | <span data-ttu-id="9475e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9475e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9475e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9475e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9475e-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9475e-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="9475e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9475e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9475e-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9475e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9475e-121">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9475e-121">End of server support</span></span><br/>    | <span data-ttu-id="9475e-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9475e-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="9475e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9475e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9475e-124"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9475e-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9475e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9475e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9475e-126">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="9475e-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9475e-127">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="9475e-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="9475e-128">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="9475e-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="9475e-129">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="9475e-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





