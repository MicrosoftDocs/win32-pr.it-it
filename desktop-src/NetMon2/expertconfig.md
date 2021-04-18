---
description: La struttura EXPERTCONFIG contiene i dati di configurazione dell'esperto. L'esperto sovrappone il membro RawConfigData con una struttura specifica dell'esperto.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Struttura EXPERTCONFIG (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305952"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="42dff-104">Struttura EXPERTCONFIG</span><span class="sxs-lookup"><span data-stu-id="42dff-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="42dff-105">La struttura **EXPERTCONFIG** contiene i dati di configurazione dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="42dff-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="42dff-106">L'esperto sovrappone il membro **RawConfigData** con una struttura specifica dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="42dff-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42dff-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="42dff-108">Members</span><span class="sxs-lookup"><span data-stu-id="42dff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="42dff-109">**RawConfigLength**</span><span class="sxs-lookup"><span data-stu-id="42dff-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="42dff-110">Lunghezza totale della struttura, inclusi i quattro byte utilizzati per il membro.</span><span class="sxs-lookup"><span data-stu-id="42dff-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="42dff-111">Network Monitor usa il valore quando la struttura viene salvata e letta da un'unità disco.</span><span class="sxs-lookup"><span data-stu-id="42dff-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="42dff-112">**RawConfigData**</span><span class="sxs-lookup"><span data-stu-id="42dff-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="42dff-113">Dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="42dff-113">Configuration data.</span></span> <span data-ttu-id="42dff-114">L'esperto deve aggiungere i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="42dff-114">The expert must add the configuration data.</span></span> <span data-ttu-id="42dff-115">Si supponga, ad esempio, di disporre di una struttura di dati simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="42dff-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="42dff-116">Si noti che **RawConfigLength** garantisce che la sovrapposizione funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="42dff-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="42dff-117">Quando si usano i dati, il codice potrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="42dff-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42dff-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42dff-118">Requirements</span></span>



| <span data-ttu-id="42dff-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="42dff-119">Requirement</span></span> | <span data-ttu-id="42dff-120">Valore</span><span class="sxs-lookup"><span data-stu-id="42dff-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42dff-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42dff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42dff-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42dff-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42dff-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42dff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42dff-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42dff-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="42dff-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42dff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="42dff-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="42dff-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




