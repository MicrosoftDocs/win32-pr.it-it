---
description: Rappresenta il tipo di informazioni nella struttura delle \_ informazioni del set di CPU di sistema \_ \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Enumerazione CPU_SET_INFORMATION_TYPE (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311994"
---
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="fae8d-103">\_Enumerazione del \_ tipo di informazioni set CPU \_</span><span class="sxs-lookup"><span data-stu-id="fae8d-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="fae8d-104">Rappresenta il tipo di informazioni nella struttura [**delle \_ \_ \_ informazioni del set di CPU di sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .</span><span class="sxs-lookup"><span data-stu-id="fae8d-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae8d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fae8d-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="fae8d-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="fae8d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fae8d-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span><span class="sxs-lookup"><span data-stu-id="fae8d-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="fae8d-108">La struttura contiene informazioni sul set di CPU.</span><span class="sxs-lookup"><span data-stu-id="fae8d-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fae8d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fae8d-109">Requirements</span></span>



| <span data-ttu-id="fae8d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae8d-110">Requirement</span></span> | <span data-ttu-id="fae8d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fae8d-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae8d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fae8d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fae8d-113">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fae8d-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="fae8d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fae8d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fae8d-115">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="fae8d-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fae8d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fae8d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae8d-117"><dt>Processthreadsapi. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fae8d-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 




