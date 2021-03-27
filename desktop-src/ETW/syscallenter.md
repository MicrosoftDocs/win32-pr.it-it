---
description: Questa classe è la classe del tipo di evento per le chiamate di sistema immettere gli eventi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Classe SysCallEnter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980079"
---
# <a name="syscallenter-class"></a><span data-ttu-id="445c7-104">Classe SysCallEnter</span><span class="sxs-lookup"><span data-stu-id="445c7-104">SysCallEnter class</span></span>

<span data-ttu-id="445c7-105">Questa classe è la classe del tipo di evento per le chiamate di sistema immettere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="445c7-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="445c7-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="445c7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="445c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="445c7-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="445c7-108">Members</span><span class="sxs-lookup"><span data-stu-id="445c7-108">Members</span></span>

<span data-ttu-id="445c7-109">La classe **SysCallEnter** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="445c7-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="445c7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="445c7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="445c7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="445c7-111">Properties</span></span>

<span data-ttu-id="445c7-112">La classe **SysCallEnter** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="445c7-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="445c7-113">**SysCallAddress**</span><span class="sxs-lookup"><span data-stu-id="445c7-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="445c7-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="445c7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="445c7-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="445c7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="445c7-116">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="445c7-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="445c7-117">Indirizzo della chiamata di funzione NT da immettere.</span><span class="sxs-lookup"><span data-stu-id="445c7-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="445c7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="445c7-118">Requirements</span></span>



| <span data-ttu-id="445c7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="445c7-119">Requirement</span></span> | <span data-ttu-id="445c7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="445c7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="445c7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="445c7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="445c7-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="445c7-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="445c7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="445c7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="445c7-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="445c7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




