---
description: Il tipo di dati TimeStamp include informazioni sulla validità dell'ora dei token di sicurezza. Il formato del valore del tipo di dati TimeStamp corrisponde a quello della struttura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: TimeStamp (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310467"
---
# <a name="timestamp"></a><span data-ttu-id="f2aa8-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="f2aa8-104">TimeStamp</span></span>

<span data-ttu-id="f2aa8-105">Il tipo di dati **timestamp** include informazioni sulla validità dell'ora dei token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f2aa8-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="f2aa8-106">Il formato del valore del tipo di dati **timestamp** corrisponde a quello della struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="f2aa8-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="f2aa8-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2aa8-107">Requirements</span></span>



| <span data-ttu-id="f2aa8-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2aa8-108">Requirement</span></span> | <span data-ttu-id="f2aa8-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f2aa8-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2aa8-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2aa8-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f2aa8-111">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2aa8-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f2aa8-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2aa8-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f2aa8-113">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2aa8-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f2aa8-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2aa8-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2aa8-115"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2aa8-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 
