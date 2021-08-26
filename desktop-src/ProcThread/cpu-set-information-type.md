---
description: Rappresenta il tipo di informazioni nella struttura SYSTEM \_ CPU \_ SET \_ INFORMATION.
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: CPU_SET_INFORMATION_TYPE enumerazione (Processthreadapi.h)
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
ms.openlocfilehash: 7c932a143553c1101d6a81bac86ba54e21603eaf80ed5d2613484bff22a7e625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101931"
---
# <a name="cpu_set_information_type-enumeration"></a>Enumerazione \_ CPU SET INFORMATION \_ \_ TYPE

Rappresenta il tipo di informazioni nella struttura [**SYSTEM \_ CPU SET \_ \_ INFORMATION.**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                       |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi.h (includere Windows.h)</dt> </dl> |



 

 




