---
title: Tipi di dati del servizio di accesso remoto (RAS. h)
description: I tipi di dati seguenti vengono usati dall'API del servizio di accesso remoto.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964186"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="ef543-105">Tipi di dati del servizio di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="ef543-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="ef543-106">I tipi di dati seguenti vengono usati dall'API del servizio di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="ef543-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="ef543-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="ef543-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="ef543-108">Oggetto [**in \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) che contiene un indirizzo IPv4.</span><span class="sxs-lookup"><span data-stu-id="ef543-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="ef543-109">Supportato in Windows Vista o versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef543-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="ef543-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="ef543-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="ef543-111">[**\_ Addr IN6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) che contiene un indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="ef543-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="ef543-112">Supportato in Windows Vista o versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef543-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef543-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef543-113">Requirements</span></span>



| <span data-ttu-id="ef543-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef543-114">Requirement</span></span> | <span data-ttu-id="ef543-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ef543-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef543-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef543-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef543-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef543-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ef543-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef543-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef543-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef543-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef543-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef543-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef543-121"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef543-121"><dt>Ras.h</dt></span></span> </dl> |



 

