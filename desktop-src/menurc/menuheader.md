---
title: Struttura MENUHEADER
description: Contiene informazioni sulla versione per la risorsa di menu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menu struttura MENUHEADER e altre risorse
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301025"
---
# <a name="menuheader-structure"></a><span data-ttu-id="068ba-105">Struttura MENUHEADER</span><span class="sxs-lookup"><span data-stu-id="068ba-105">MENUHEADER structure</span></span>

<span data-ttu-id="068ba-106">Contiene informazioni sulla versione per la risorsa di menu.</span><span class="sxs-lookup"><span data-stu-id="068ba-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="068ba-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="068ba-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="068ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="068ba-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="068ba-109">Members</span><span class="sxs-lookup"><span data-stu-id="068ba-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="068ba-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="068ba-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="068ba-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="068ba-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="068ba-112">Numero di versione del modello di menu.</span><span class="sxs-lookup"><span data-stu-id="068ba-112">The version number of the menu template.</span></span> <span data-ttu-id="068ba-113">Questo membro deve essere uguale a zero per indicare che si tratta di [**un \_ menu RT**](/windows/desktop/menurc/resource-types) creato con un modello di menu standard.</span><span class="sxs-lookup"><span data-stu-id="068ba-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="068ba-114">**cbHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="068ba-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="068ba-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="068ba-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="068ba-116">Dimensioni dell'intestazione del modello di menu.</span><span class="sxs-lookup"><span data-stu-id="068ba-116">The size of the menu template header.</span></span> <span data-ttu-id="068ba-117">Questo valore è zero per i menu creati con un modello di menu standard.</span><span class="sxs-lookup"><span data-stu-id="068ba-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="068ba-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="068ba-118">Requirements</span></span>



| <span data-ttu-id="068ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="068ba-119">Requirement</span></span> | <span data-ttu-id="068ba-120">Valore</span><span class="sxs-lookup"><span data-stu-id="068ba-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="068ba-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="068ba-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="068ba-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="068ba-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="068ba-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="068ba-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="068ba-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="068ba-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="068ba-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="068ba-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="068ba-127">**\_intestazione del modello menuex \_**</span><span class="sxs-lookup"><span data-stu-id="068ba-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="068ba-128">**\_elemento del modello menuex \_**</span><span class="sxs-lookup"><span data-stu-id="068ba-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="068ba-129">**MENUITEMTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="068ba-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="068ba-130">**MENUITEMTEMPLATEHEADER**</span><span class="sxs-lookup"><span data-stu-id="068ba-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="068ba-131">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="068ba-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="068ba-132">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="068ba-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="068ba-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="068ba-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="068ba-134">Risorse</span><span class="sxs-lookup"><span data-stu-id="068ba-134">Resources</span></span>](resources.md)
</dt> </dl>

 

