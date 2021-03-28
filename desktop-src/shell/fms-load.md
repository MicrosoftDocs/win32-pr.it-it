---
description: Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di file Manager. La struttura fornisce inoltre un valore Delta che può essere utilizzato dalla DLL di estensione per modificare il menu personalizzato dopo che il menu è stato caricato da file Manager.
title: Struttura FMS_LOAD (Wfext. h)
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
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977087"
---
# <a name="fms_load-structure"></a><span data-ttu-id="55053-104">\_Struttura di caricamento FMS</span><span class="sxs-lookup"><span data-stu-id="55053-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="55053-105">Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di file Manager.</span><span class="sxs-lookup"><span data-stu-id="55053-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="55053-106">La struttura fornisce inoltre un valore Delta che può essere utilizzato dalla DLL di estensione per modificare il menu personalizzato dopo che il menu è stato caricato da file Manager.</span><span class="sxs-lookup"><span data-stu-id="55053-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="55053-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55053-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="55053-108">Members</span><span class="sxs-lookup"><span data-stu-id="55053-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="55053-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="55053-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="55053-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="55053-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="55053-111">Lunghezza, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="55053-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="55053-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="55053-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="55053-113">Tipo: **TCHAR \[ il \_ testo del menu \_ \] Len**</span><span class="sxs-lookup"><span data-stu-id="55053-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="55053-114">Nome con terminazione null per una voce di menu visualizzata sulla barra dei menu in gestione file.</span><span class="sxs-lookup"><span data-stu-id="55053-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="55053-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="55053-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="55053-116">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="55053-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="55053-117">Identificatore del menu popup aggiunto alla barra dei menu in gestione file.</span><span class="sxs-lookup"><span data-stu-id="55053-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="55053-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="55053-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="55053-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="55053-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="55053-120">Valore delta della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55053-120">The menu item delta value.</span></span> <span data-ttu-id="55053-121">Per evitare conflitti con le proprie voci di menu, gestione file consente di rinumerare gli identificatori delle voci di menu nel menu popup identificato dal membro **HMENU** aggiungendo questo valore Delta a ogni identificatore.</span><span class="sxs-lookup"><span data-stu-id="55053-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="55053-122">Una DLL di estensione che deve modificare una voce di menu deve identificare l'elemento aggiungendo il valore delta all'identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="55053-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="55053-123">Il valore di questo membro può variare da sessione a sessione.</span><span class="sxs-lookup"><span data-stu-id="55053-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55053-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55053-124">Requirements</span></span>



| <span data-ttu-id="55053-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="55053-125">Requirement</span></span> | <span data-ttu-id="55053-126">Valore</span><span class="sxs-lookup"><span data-stu-id="55053-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55053-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55053-127">Minimum supported client</span></span><br/> | <span data-ttu-id="55053-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55053-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="55053-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55053-129">Minimum supported server</span></span><br/> | <span data-ttu-id="55053-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55053-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="55053-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55053-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="55053-132"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="55053-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55053-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55053-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55053-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="55053-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




