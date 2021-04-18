---
description: Handle per un buffer di stringa modificabile che è possibile utilizzare per creare un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (HSTRING. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307082"
---
# <a name="hstring_buffer"></a><span data-ttu-id="90ea1-103">\_buffer HString</span><span class="sxs-lookup"><span data-stu-id="90ea1-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="90ea1-104">Handle per un buffer di stringa modificabile che è possibile utilizzare per creare un [**HString**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="90ea1-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="90ea1-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="90ea1-105">Remarks</span></span>

<span data-ttu-id="90ea1-106">**HString \_ Il BUFFER** rappresenta un buffer di stringa che è possibile modificare prima di convertirlo in un [**HString**](hstring.md)non modificabile.</span><span class="sxs-lookup"><span data-stu-id="90ea1-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="90ea1-107">Chiamare la funzione [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) per creare un **\_ buffer HString**.</span><span class="sxs-lookup"><span data-stu-id="90ea1-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="90ea1-108">Chiamare [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) per convertire un **\_ buffer HString** in un [**HString**](hstring.md)non modificabile.</span><span class="sxs-lookup"><span data-stu-id="90ea1-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90ea1-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90ea1-109">Requirements</span></span>



| <span data-ttu-id="90ea1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ea1-110">Requirement</span></span> | <span data-ttu-id="90ea1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="90ea1-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90ea1-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ea1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="90ea1-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="90ea1-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="90ea1-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90ea1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="90ea1-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90ea1-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="90ea1-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90ea1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ea1-117"><dt>HSTRING. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ea1-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ea1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90ea1-118">See also</span></span>

<dl> <span data-ttu-id="90ea1-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="90ea1-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="90ea1-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="90ea1-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="90ea1-121">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="90ea1-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="90ea1-122">**WindowsPromoteStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="90ea1-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
