---
description: La struttura PROTOCOLTABLE contiene un elenco di protocolli.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Struttura PROTOCOLTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315451"
---
# <a name="protocoltable-structure"></a><span data-ttu-id="ad7d1-103">Struttura PROTOCOLTABLE</span><span class="sxs-lookup"><span data-stu-id="ad7d1-103">PROTOCOLTABLE structure</span></span>

<span data-ttu-id="ad7d1-104">La struttura **PROTOCOLTABLE** contiene un elenco di protocolli.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-104">The **PROTOCOLTABLE** structure contains a list of protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad7d1-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a><span data-ttu-id="ad7d1-106">Members</span><span class="sxs-lookup"><span data-stu-id="ad7d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad7d1-107">**nProtocols**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-107">**nProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="ad7d1-108">Numero di protocolli abilitati.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-108">Number of protocols that are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ad7d1-109">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-109">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="ad7d1-110">Matrice di handle per i protocolli abilitati.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-110">Array of handles to enabled protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad7d1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad7d1-111">Requirements</span></span>



| <span data-ttu-id="ad7d1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad7d1-112">Requirement</span></span> | <span data-ttu-id="ad7d1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ad7d1-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7d1-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad7d1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7d1-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad7d1-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ad7d1-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad7d1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7d1-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad7d1-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ad7d1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad7d1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad7d1-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7d1-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




