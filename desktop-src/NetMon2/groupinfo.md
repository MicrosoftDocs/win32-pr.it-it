---
description: Associa un nome di gruppo e il relativo handle.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Struttura GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305891"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="7dd64-103">Struttura GROUPINFO</span><span class="sxs-lookup"><span data-stu-id="7dd64-103">GROUPINFO structure</span></span>

<span data-ttu-id="7dd64-104">La struttura **GROUPINFO** associa un nome di gruppo e il relativo handle.</span><span class="sxs-lookup"><span data-stu-id="7dd64-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd64-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dd64-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="7dd64-106">Members</span><span class="sxs-lookup"><span data-stu-id="7dd64-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dd64-107">**szGroupName**</span><span class="sxs-lookup"><span data-stu-id="7dd64-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="7dd64-108">Valore incrementato di una matrice nella struttura **GroupName** .</span><span class="sxs-lookup"><span data-stu-id="7dd64-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7dd64-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="7dd64-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="7dd64-110">Handle per un gruppo.</span><span class="sxs-lookup"><span data-stu-id="7dd64-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dd64-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dd64-111">Requirements</span></span>



| <span data-ttu-id="7dd64-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dd64-112">Requirement</span></span> | <span data-ttu-id="7dd64-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7dd64-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd64-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dd64-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd64-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dd64-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7dd64-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dd64-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd64-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dd64-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7dd64-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dd64-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd64-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd64-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




