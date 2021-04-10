---
title: Tipi di dati DNS (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Altre informazioni su: tipi di dati DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231543"
---
# <a name="dns-data-types"></a><span data-ttu-id="15c4c-104">Tipi di dati DNS</span><span class="sxs-lookup"><span data-stu-id="15c4c-104">DNS Data Types</span></span>

<span data-ttu-id="15c4c-105">Per DNS sono definiti i tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="15c4c-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="15c4c-106">**\_Indirizzo IP4**</span><span class="sxs-lookup"><span data-stu-id="15c4c-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="15c4c-107">Valore che rappresenta un indirizzo IPv4 (Internet Protocol versione 4).</span><span class="sxs-lookup"><span data-stu-id="15c4c-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="15c4c-108">Ad esempio, l'indirizzo IPv4 decimale punteggiato, **127.0.0.1**, viene rappresentato nell'ordine dei byte dell'host come **0x7F000001**.</span><span class="sxs-lookup"><span data-stu-id="15c4c-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15c4c-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15c4c-109">Requirements</span></span>



| <span data-ttu-id="15c4c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c4c-110">Requirement</span></span> | <span data-ttu-id="15c4c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="15c4c-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15c4c-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15c4c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="15c4c-113">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="15c4c-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15c4c-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15c4c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="15c4c-115">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="15c4c-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15c4c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15c4c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="15c4c-117"><dt>Windns. h</dt></span><span class="sxs-lookup"><span data-stu-id="15c4c-117"><dt>Windns.h</dt></span></span> </dl> |



 

 





