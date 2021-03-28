---
description: Classe padre dalla quale vengono derivate tutte le classi di traccia degli eventi di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Classe MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977818"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="bda77-104">\_Classe MSNT SystemTrace</span><span class="sxs-lookup"><span data-stu-id="bda77-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="bda77-105">Classe padre dalla quale vengono derivate tutte le classi di traccia degli eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="bda77-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="bda77-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="bda77-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda77-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bda77-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="bda77-108">Members</span><span class="sxs-lookup"><span data-stu-id="bda77-108">Members</span></span>

<span data-ttu-id="bda77-109">La **classe \_ SystemTrace di MSNT** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bda77-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="bda77-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bda77-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bda77-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bda77-111">Properties</span></span>

<span data-ttu-id="bda77-112">La **classe \_ SystemTrace di MSNT** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bda77-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bda77-113">**Flag**</span><span class="sxs-lookup"><span data-stu-id="bda77-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bda77-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bda77-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bda77-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bda77-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda77-116">Qualificatori: **DefineValues {" \_ \_ processo flag di traccia eventi \_ ", " \_ \_ thread flag \_ di traccia eventi", \_ " \_ \_ caricamento immagine flag di traccia eventi \_ ", " \_ \_ \_ contatori processo flag di traccia eventi \_ ", " \_ flag di traccia evento \_ \_ CSWITCH", " \_ flag di traccia evento \_ \_ DPC", " \_ \_ interrupt flag di traccia evento \_ ", " \_ flag di traccia eventi \_ \_ SYSTEMCALL", "flag di traccia eventi i/o \_ \_ \_ disco \_ ", "flag di traccia eventi i/o \_ \_ \_ \_ file disco \_ ", " \_ flag di traccia evento \_ \_ disco \_ io \_ init", "Event \_ trace \_ flag \_ dispatcher", "EVENT \_ trace \_ flag \_ Memory \_ Page \_ fault", "Event \_ trace flag memoria hardware", \_ \_ \_ \_ "EVENT \_ trace \_ flag \_ virtual \_ Alloc", "Event \_ trace \_ flag \_ Network \_ tcpip" \_ Registro di traccia eventi registro di \_ \_ sistema "," \_ flag di traccia evento \_ \_ ALPC "," \_ flag di traccia evento \_ \_ split \_ io "," \_ \_ driver di traccia di traccia eventi \_ "," \_ profilo contrassegno di traccia eventi "," i/o file flag di traccia eventi " \_ \_ \_ \_ \_ \_ ," \_ traccia eventi \_ flag \_ file \_ io \_ init "}**, **ValueMap {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "** 0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}</span><span class="sxs-lookup"><span data-stu-id="bda77-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="bda77-117">Abilita flag che indica i provider di kernel abilitati.</span><span class="sxs-lookup"><span data-stu-id="bda77-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bda77-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda77-118">Requirements</span></span>



| <span data-ttu-id="bda77-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda77-119">Requirement</span></span> | <span data-ttu-id="bda77-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bda77-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bda77-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda77-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bda77-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bda77-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bda77-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda77-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bda77-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bda77-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




