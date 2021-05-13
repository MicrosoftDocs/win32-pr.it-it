---
description: Contiene informazioni utilizzate da File Manager per aggiungere una stringa della Guida per un menu o una voce di comando della barra degli strumenti.
title: FMS_HELPSTRING struttura (Wfext.h)
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
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842212"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="998bd-103">Struttura FMS \_ HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="998bd-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="998bd-104">Contiene informazioni utilizzate da File Manager per aggiungere una stringa della Guida per un menu o una voce di comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="998bd-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="998bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="998bd-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="998bd-106">Members</span><span class="sxs-lookup"><span data-stu-id="998bd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="998bd-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="998bd-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="998bd-108">Tipo: **INT**</span><span class="sxs-lookup"><span data-stu-id="998bd-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="998bd-109">Identificatore dell'elemento di comando.</span><span class="sxs-lookup"><span data-stu-id="998bd-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="998bd-110">**Hmenu**</span><span class="sxs-lookup"><span data-stu-id="998bd-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="998bd-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="998bd-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="998bd-112">Identificatore della barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="998bd-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="998bd-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="998bd-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="998bd-114">Tipo: **\_ \_ wchar \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="998bd-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="998bd-115">Stringa con terminazione Null che riceve il testo della Guida.</span><span class="sxs-lookup"><span data-stu-id="998bd-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="998bd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="998bd-116">Requirements</span></span>



| <span data-ttu-id="998bd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="998bd-117">Requirement</span></span> | <span data-ttu-id="998bd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="998bd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="998bd-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="998bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="998bd-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="998bd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="998bd-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="998bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="998bd-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="998bd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="998bd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="998bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="998bd-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="998bd-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="998bd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="998bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998bd-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="998bd-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="998bd-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="998bd-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




