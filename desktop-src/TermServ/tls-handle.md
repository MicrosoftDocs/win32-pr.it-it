---
title: TLS_HANDLE
description: Rappresenta un handle per un server licenze Desktop remoto.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740714"
---
# <a name="tls_handle"></a><span data-ttu-id="0f057-104">\_handle TLS</span><span class="sxs-lookup"><span data-stu-id="0f057-104">TLS\_HANDLE</span></span>

<span data-ttu-id="0f057-105">Rappresenta un handle per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0f057-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="0f057-106">Questo handle viene restituito dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="0f057-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="0f057-107">A questo tipo di dati non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="0f057-107">This data type has no associated header file.</span></span> <span data-ttu-id="0f057-108">Per usarlo, è necessario definirlo come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0f057-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="0f057-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f057-109">Requirements</span></span>



| <span data-ttu-id="0f057-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f057-110">Requirement</span></span> | <span data-ttu-id="0f057-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0f057-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0f057-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f057-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0f057-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f057-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0f057-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f057-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0f057-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f057-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f057-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f057-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f057-117">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="0f057-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="0f057-118">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="0f057-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





