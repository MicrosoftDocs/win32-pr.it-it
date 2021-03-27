---
description: La \_ classe NIC HWConfig è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Classe HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058118"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="1c84e-104">\_Classe NIC HWConfig</span><span class="sxs-lookup"><span data-stu-id="1c84e-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="1c84e-105">La **classe \_ NIC HWConfig** è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1c84e-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="1c84e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="1c84e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c84e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c84e-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="1c84e-108">Members</span><span class="sxs-lookup"><span data-stu-id="1c84e-108">Members</span></span>

<span data-ttu-id="1c84e-109">La **classe \_ NIC HWConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c84e-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="1c84e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c84e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c84e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c84e-111">Properties</span></span>

<span data-ttu-id="1c84e-112">La **classe \_ NIC HWConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c84e-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c84e-113">NICName</span><span class="sxs-lookup"><span data-stu-id="1c84e-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c84e-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1c84e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c84e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c84e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c84e-116">Qualificatori: WmiDataId (1), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="1c84e-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="1c84e-117">Nome della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1c84e-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c84e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c84e-118">Requirements</span></span>



| <span data-ttu-id="1c84e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c84e-119">Requirement</span></span> | <span data-ttu-id="1c84e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1c84e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="1c84e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c84e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c84e-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1c84e-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c84e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c84e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c84e-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1c84e-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="1c84e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c84e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c84e-126">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="1c84e-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




