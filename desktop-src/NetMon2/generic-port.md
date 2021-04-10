---
description: Contiene un numero di porta usato per i protocolli IP o IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: Unione GENERIC_PORT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966475"
---
# <a name="generic_port-union"></a><span data-ttu-id="0a801-103">\_Unione porta generica</span><span class="sxs-lookup"><span data-stu-id="0a801-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="0a801-104">La **struttura \_ porta generica** contiene un numero di porta usato per i protocolli IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="0a801-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a801-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a801-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="0a801-106">Members</span><span class="sxs-lookup"><span data-stu-id="0a801-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a801-107">**IPPort**</span><span class="sxs-lookup"><span data-stu-id="0a801-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="0a801-108">Numero di porta IP compilato.</span><span class="sxs-lookup"><span data-stu-id="0a801-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="0a801-109">**ByteSwappedIPXPort**</span><span class="sxs-lookup"><span data-stu-id="0a801-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="0a801-110">Numero di porta IPX compilato.</span><span class="sxs-lookup"><span data-stu-id="0a801-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a801-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a801-111">Requirements</span></span>



| <span data-ttu-id="0a801-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a801-112">Requirement</span></span> | <span data-ttu-id="0a801-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0a801-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0a801-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a801-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0a801-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a801-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0a801-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a801-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0a801-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a801-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0a801-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a801-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a801-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a801-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




