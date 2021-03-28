---
description: Questi tipi di dati possono essere utilizzati per specificare il tipo di un valore del registro di sistema.
title: Tipi di dati del registro di sistema (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996593"
---
# <a name="registry-data-types"></a><span data-ttu-id="fb2ca-103">Tipi di dati del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="fb2ca-103">Registry Data Types</span></span>

<span data-ttu-id="fb2ca-104">Questi tipi di dati possono essere utilizzati per specificare il tipo di un valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="fb2ca-105">Costante</span><span class="sxs-lookup"><span data-stu-id="fb2ca-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="fb2ca-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb2ca-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="fb2ca-107"><dt>**REG \_ binario**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="fb2ca-108">Dati binari in qualsiasi forma.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="fb2ca-109"><dt>**REG \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="fb2ca-110">numero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="fb2ca-111"><dt>**REG \_ QWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="fb2ca-112">numero a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="fb2ca-113"><dt>**\_ \_ Little Endian reg \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="fb2ca-114">numero a 32 bit in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="fb2ca-115">Equivale a **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="fb2ca-116">In formato little-endian, un valore multibyte viene archiviato in memoria dal byte più basso, ovvero "estremità minima", al byte più alto.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="fb2ca-117">Il valore 0x12345678., ad esempio, viene archiviato come (0x78 0x56 0x34 0x12) in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="fb2ca-118"><dt>**REG \_ QWORD \_ Little \_ endian**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="fb2ca-119">Numero a 64 bit in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="fb2ca-120">Equivale a **reg \_ QWORD**.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="fb2ca-121"><dt>**REG \_ DWORD \_ Big \_ endian**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="fb2ca-122">numero a 32 bit nel formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="fb2ca-123">Nel formato big-endian, un valore multibyte viene archiviato in memoria dal byte più alto ("Big end") al byte più basso.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="fb2ca-124">Il valore 0x12345678., ad esempio, viene archiviato come (0x12 0x34 0x56 0x78) nel formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="fb2ca-125"><dt>**REG \_ Espandi \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="fb2ca-126">Stringa con terminazione null che contiene riferimenti non espansi a variabili di ambiente (ad esempio, "% PATH%").</span><span class="sxs-lookup"><span data-stu-id="fb2ca-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="fb2ca-127">Si tratta di una stringa Unicode o ANSI, a seconda che si usino le funzioni Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="fb2ca-128"><dt>**\_collegamento reg**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="fb2ca-129">Collegamento simbolico Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="fb2ca-130"><dt>**REG \_ - \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="fb2ca-131">Matrice di stringhe con terminazione null che terminano con due caratteri null.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="fb2ca-132"><dt>**REG \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="fb2ca-133">Nessun tipo di valore definito.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="fb2ca-134"><dt>**\_elenco delle risorse reg \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="fb2ca-135">Elenco delle risorse del driver del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="fb2ca-136"><dt>**REG \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="fb2ca-137">Stringa con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-137">Null-terminated string.</span></span> <span data-ttu-id="fb2ca-138">Si tratta di una stringa Unicode o ANSI, a seconda che si usino le funzioni Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="fb2ca-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="fb2ca-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb2ca-139">Requirements</span></span>



| <span data-ttu-id="fb2ca-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb2ca-140">Requirement</span></span> | <span data-ttu-id="fb2ca-141">Valore</span><span class="sxs-lookup"><span data-stu-id="fb2ca-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2ca-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb2ca-142">Header</span></span><br/> | <dl> <span data-ttu-id="fb2ca-143"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ca-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




