---
title: Struttura Connections (NapEnforcementClient. h)
description: Contiene informazioni sull'elenco di connessioni gestite da un Enforcer.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Struttura delle connessioni NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964985"
---
# <a name="connections-structure"></a><span data-ttu-id="c5930-104">Struttura Connections</span><span class="sxs-lookup"><span data-stu-id="c5930-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="c5930-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="c5930-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c5930-106">La struttura **Connections** contiene informazioni sull'elenco di connessioni gestite da un Enforcer.</span><span class="sxs-lookup"><span data-stu-id="c5930-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5930-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5930-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="c5930-108">Members</span><span class="sxs-lookup"><span data-stu-id="c5930-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5930-109">**count**</span><span class="sxs-lookup"><span data-stu-id="c5930-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="c5930-110">Il numero di connessioni attive attualmente gestite da un Enforcer compreso nell'intervallo 0 (zero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c5930-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5930-111">**connessioni**</span><span class="sxs-lookup"><span data-stu-id="c5930-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="c5930-112">Puntatore COM a un elenco di interfacce [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) che rappresentano le connessioni client.</span><span class="sxs-lookup"><span data-stu-id="c5930-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5930-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5930-113">Requirements</span></span>



| <span data-ttu-id="c5930-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5930-114">Requirement</span></span> | <span data-ttu-id="c5930-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c5930-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5930-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5930-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c5930-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5930-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5930-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5930-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c5930-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5930-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5930-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5930-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5930-121"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5930-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5930-122">IDL</span><span class="sxs-lookup"><span data-stu-id="c5930-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5930-123"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5930-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5930-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5930-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5930-125">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="c5930-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="c5930-126">Strutture NAP</span><span class="sxs-lookup"><span data-stu-id="c5930-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="c5930-127">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c5930-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





