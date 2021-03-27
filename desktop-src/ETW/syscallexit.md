---
description: Questa classe è la classe del tipo di evento per gli eventi di uscita delle chiamate di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Classe SysCallExit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980074"
---
# <a name="syscallexit-class"></a><span data-ttu-id="b3b29-104">Classe SysCallExit</span><span class="sxs-lookup"><span data-stu-id="b3b29-104">SysCallExit class</span></span>

<span data-ttu-id="b3b29-105">Questa classe è la classe del tipo di evento per gli eventi di uscita delle chiamate di sistema.</span><span class="sxs-lookup"><span data-stu-id="b3b29-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="b3b29-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b3b29-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b29-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3b29-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="b3b29-108">Members</span><span class="sxs-lookup"><span data-stu-id="b3b29-108">Members</span></span>

<span data-ttu-id="b3b29-109">La classe **SysCallExit** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3b29-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="b3b29-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3b29-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3b29-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3b29-111">Properties</span></span>

<span data-ttu-id="b3b29-112">La classe **SysCallExit** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3b29-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3b29-113">**SysCallNtStatus**</span><span class="sxs-lookup"><span data-stu-id="b3b29-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3b29-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3b29-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3b29-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3b29-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3b29-116">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="b3b29-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b3b29-117">Codice di stato restituito dalla chiamata di sistema NT.</span><span class="sxs-lookup"><span data-stu-id="b3b29-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3b29-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3b29-118">Requirements</span></span>



| <span data-ttu-id="b3b29-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b29-119">Requirement</span></span> | <span data-ttu-id="b3b29-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b3b29-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3b29-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3b29-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b29-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3b29-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3b29-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3b29-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b29-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3b29-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




