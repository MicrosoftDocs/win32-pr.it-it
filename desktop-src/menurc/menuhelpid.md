---
title: Struttura MENUHELPID
description: Contiene i dati finali scritti nella risorsa di \_ menu RT per un menu o un sottomenu se il membro resInfo della struttura POPUPMENUITEM è impostato su un \_ popup fabbisogno.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menu struttura MENUHELPID e altre risorse
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302527"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="b06da-104">Struttura MENUHELPID</span><span class="sxs-lookup"><span data-stu-id="b06da-104">MENUHELPID structure</span></span>

<span data-ttu-id="b06da-105">Contiene i dati finali scritti nella risorsa [**di \_ menu RT**](/windows/desktop/menurc/resource-types) per un menu o un sottomenu se il membro **resInfo** della struttura [**POPUPMENUITEM**](popupmenuitem.md) è impostato su **un \_ popup fabbisogno**.</span><span class="sxs-lookup"><span data-stu-id="b06da-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="b06da-106">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="b06da-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b06da-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="b06da-108">Members</span><span class="sxs-lookup"><span data-stu-id="b06da-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b06da-109">**helpID**</span><span class="sxs-lookup"><span data-stu-id="b06da-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="b06da-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b06da-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b06da-111">Identificatore usato per identificare il menu durante l'elaborazione della [**\_ Guida di WM**](/windows/desktop/shell/wm-help) .</span><span class="sxs-lookup"><span data-stu-id="b06da-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b06da-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b06da-112">Requirements</span></span>



| <span data-ttu-id="b06da-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b06da-113">Requirement</span></span> | <span data-ttu-id="b06da-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b06da-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b06da-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b06da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b06da-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b06da-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b06da-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b06da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b06da-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b06da-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b06da-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b06da-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b06da-120">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b06da-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b06da-121">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="b06da-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="b06da-122">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="b06da-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="b06da-123">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b06da-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b06da-124">Risorse</span><span class="sxs-lookup"><span data-stu-id="b06da-124">Resources</span></span>](resources.md)
</dt> </dl>

 

