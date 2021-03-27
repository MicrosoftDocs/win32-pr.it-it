---
description: Inviato a una DLL di estensione quando l'utente seleziona il menu per l'estensione dalla barra dei menu di gestione file. L'estensione può usare questa notifica per inizializzare le voci di menu.
title: Messaggio FMEVENT_INITMENU (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225798"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="6db89-104">\_Messaggio FMEVENT INITMENU</span><span class="sxs-lookup"><span data-stu-id="6db89-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="6db89-105">Inviato a una DLL di estensione quando l'utente seleziona il menu per l'estensione dalla barra dei menu di gestione file.</span><span class="sxs-lookup"><span data-stu-id="6db89-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="6db89-106">L'estensione può usare questa notifica per inizializzare le voci di menu.</span><span class="sxs-lookup"><span data-stu-id="6db89-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="6db89-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6db89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db89-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6db89-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6db89-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6db89-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6db89-110">*HMENU*</span><span class="sxs-lookup"><span data-stu-id="6db89-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="6db89-111">Handle per la barra dei menu di gestione file.</span><span class="sxs-lookup"><span data-stu-id="6db89-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db89-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6db89-112">Return value</span></span>

<span data-ttu-id="6db89-113">Una DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6db89-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="6db89-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6db89-114">Remarks</span></span>

<span data-ttu-id="6db89-115">Una DLL di estensione riceve questo messaggio solo quando l'utente seleziona il menu di primo livello.</span><span class="sxs-lookup"><span data-stu-id="6db89-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="6db89-116">Se l'estensione contiene sottomenu, è necessario inizializzarli nello stesso momento in cui viene inizializzato il menu di primo livello.</span><span class="sxs-lookup"><span data-stu-id="6db89-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db89-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6db89-117">Requirements</span></span>



| <span data-ttu-id="6db89-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db89-118">Requirement</span></span> | <span data-ttu-id="6db89-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6db89-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6db89-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6db89-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6db89-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6db89-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6db89-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6db89-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6db89-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6db89-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6db89-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6db89-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db89-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db89-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db89-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6db89-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db89-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="6db89-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




