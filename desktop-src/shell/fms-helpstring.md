---
description: Contiene informazioni utilizzate da Gestione file per aggiungere una stringa della Guida per un elemento di comando di menu o barre degli strumenti.
title: Struttura FMS_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994741"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="f1e07-103">\_Struttura HELPSTRING FMS</span><span class="sxs-lookup"><span data-stu-id="f1e07-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="f1e07-104">Contiene informazioni utilizzate da Gestione file per aggiungere una stringa della Guida per un elemento di comando di menu o barre degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f1e07-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e07-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="f1e07-106">Members</span><span class="sxs-lookup"><span data-stu-id="f1e07-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1e07-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="f1e07-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="f1e07-108">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f1e07-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="f1e07-109">Identificatore dell'elemento di comando.</span><span class="sxs-lookup"><span data-stu-id="f1e07-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="f1e07-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="f1e07-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="f1e07-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="f1e07-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="f1e07-112">Identificatore della barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="f1e07-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="f1e07-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="f1e07-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="f1e07-114">Tipo: **\_ \_ WCHAR \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="f1e07-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="f1e07-115">Stringa con terminazione null che riceve il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="f1e07-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1e07-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e07-116">Requirements</span></span>



| <span data-ttu-id="f1e07-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e07-117">Requirement</span></span> | <span data-ttu-id="f1e07-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e07-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e07-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e07-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1e07-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f1e07-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e07-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1e07-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f1e07-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1e07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e07-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e07-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e07-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1e07-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e07-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="f1e07-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="f1e07-127">**\_HELPMENUITEM FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="f1e07-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




