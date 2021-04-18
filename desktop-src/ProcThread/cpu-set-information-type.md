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
# <a name="cpu_set_information_type-enumeration"></a>\_Enumerazione del \_ tipo di informazioni set CPU \_

Rappresenta il tipo di informazioni nella struttura [**delle \_ \_ \_ informazioni del set di CPU di sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .

## <a name="syntax"></a>Sintassi


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**
</dt> <dd>

La struttura contiene informazioni sul set di CPU.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi. h (include Windows. h)</dt> </dl> |



 

 




