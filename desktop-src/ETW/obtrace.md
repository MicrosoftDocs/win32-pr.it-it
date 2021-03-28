---
description: Rappresenta la classe padre dalla quale vengono derivate tutte le classi di traccia degli eventi di gestione oggetti.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Classe ObTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757661"
---
# <a name="obtrace-class"></a><span data-ttu-id="7a4cb-103">Classe ObTrace</span><span class="sxs-lookup"><span data-stu-id="7a4cb-103">ObTrace class</span></span>

<span data-ttu-id="7a4cb-104">Rappresenta la classe padre dalla quale vengono derivate tutte le classi di traccia degli eventi di gestione oggetti.</span><span class="sxs-lookup"><span data-stu-id="7a4cb-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="7a4cb-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7a4cb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4cb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a4cb-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7a4cb-107">Members</span><span class="sxs-lookup"><span data-stu-id="7a4cb-107">Members</span></span>

<span data-ttu-id="7a4cb-108">La classe **ObTrace** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="7a4cb-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a4cb-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a4cb-109">Remarks</span></span>

<span data-ttu-id="7a4cb-110">Per abilitare la traccia eventi di gestione oggetti, chiamare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) con il parametro *InformationClass* uguale al valore di enumerazione della classe di [**\_ informazioni \_ di traccia**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** e il membro **EnableFlags** della struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) uguale all' **\_ \_ handle ob Perf** (0x80000040).</span><span class="sxs-lookup"><span data-stu-id="7a4cb-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4cb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a4cb-111">Requirements</span></span>



| <span data-ttu-id="7a4cb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a4cb-112">Requirement</span></span> | <span data-ttu-id="7a4cb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7a4cb-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4cb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a4cb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4cb-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7a4cb-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7a4cb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a4cb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4cb-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7a4cb-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a4cb-118">MOF</span><span class="sxs-lookup"><span data-stu-id="7a4cb-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a4cb-119"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a4cb-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
