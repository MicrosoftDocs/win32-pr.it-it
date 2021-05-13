---
description: Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di File Manager. La struttura fornisce anche un valore delta che la DLL di estensione può usare per modificare il menu personalizzato dopo che File Manager ha caricato il menu.
title: FMS_LOAD struttura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842192"
---
# <a name="fms_load-structure"></a><span data-ttu-id="4a8da-104">Struttura FMS \_ LOAD</span><span class="sxs-lookup"><span data-stu-id="4a8da-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="4a8da-105">Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di File Manager.</span><span class="sxs-lookup"><span data-stu-id="4a8da-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="4a8da-106">La struttura fornisce anche un valore delta che la DLL di estensione può usare per modificare il menu personalizzato dopo che File Manager ha caricato il menu.</span><span class="sxs-lookup"><span data-stu-id="4a8da-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a8da-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="4a8da-108">Members</span><span class="sxs-lookup"><span data-stu-id="4a8da-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a8da-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="4a8da-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="4a8da-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a8da-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4a8da-111">Lunghezza, in byte, della struttura .</span><span class="sxs-lookup"><span data-stu-id="4a8da-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a8da-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="4a8da-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="4a8da-113">Tipo: **TCHAR \[ MENU TEXT \_ \_ LEN \]**</span><span class="sxs-lookup"><span data-stu-id="4a8da-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="4a8da-114">Nome con terminazione Null per una voce di menu visualizzata sulla barra dei menu in File Manager.</span><span class="sxs-lookup"><span data-stu-id="4a8da-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="4a8da-115">**Hmenu**</span><span class="sxs-lookup"><span data-stu-id="4a8da-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="4a8da-116">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="4a8da-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="4a8da-117">Identificatore del menu a comparsa aggiunto alla barra dei menu in File Manager.</span><span class="sxs-lookup"><span data-stu-id="4a8da-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="4a8da-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="4a8da-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="4a8da-119">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="4a8da-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="4a8da-120">Valore delta della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="4a8da-120">The menu item delta value.</span></span> <span data-ttu-id="4a8da-121">Per evitare conflitti con le proprie voci di menu, File Manager rinumera gli identificatori delle voci di menu nel menu a comparsa identificato dal membro **hMenu** aggiungendo questo valore delta a ogni identificatore.</span><span class="sxs-lookup"><span data-stu-id="4a8da-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="4a8da-122">Una DLL di estensione che deve modificare una voce di menu deve identificare la voce aggiungendo il valore delta all'identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="4a8da-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="4a8da-123">Il valore di questo membro può variare da sessione a sessione.</span><span class="sxs-lookup"><span data-stu-id="4a8da-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a8da-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a8da-124">Requirements</span></span>



| <span data-ttu-id="4a8da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a8da-125">Requirement</span></span> | <span data-ttu-id="4a8da-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4a8da-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8da-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a8da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8da-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a8da-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4a8da-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a8da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8da-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a8da-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a8da-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a8da-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a8da-132"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a8da-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a8da-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a8da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8da-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="4a8da-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




