---
description: La struttura CONFIGUREDEXPERT associa un esperto ai dati di configurazione.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Struttura CONFIGUREDEXPERT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231723"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="1e49a-103">Struttura CONFIGUREDEXPERT</span><span class="sxs-lookup"><span data-stu-id="1e49a-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="1e49a-104">La struttura **CONFIGUREDEXPERT** associa un esperto ai dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1e49a-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e49a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e49a-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="1e49a-106">Members</span><span class="sxs-lookup"><span data-stu-id="1e49a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e49a-107">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="1e49a-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="1e49a-108">Handle per un esperto.</span><span class="sxs-lookup"><span data-stu-id="1e49a-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="1e49a-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="1e49a-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1e49a-110">Valori dei flag di avvio dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="1e49a-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="1e49a-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="1e49a-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="1e49a-112">Puntatore a una struttura [**EXPERTCONFIG**](expertconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1e49a-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e49a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e49a-113">Requirements</span></span>



| <span data-ttu-id="1e49a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e49a-114">Requirement</span></span> | <span data-ttu-id="1e49a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1e49a-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e49a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e49a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e49a-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e49a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1e49a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e49a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e49a-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e49a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1e49a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e49a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e49a-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e49a-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 




