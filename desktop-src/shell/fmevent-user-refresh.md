---
description: Inviato a una DLL di estensione quando l'utente sceglie il comando Aggiorna dal menu Visualizza in File Manager. L'estensione può usare questa notifica per aggiornare il relativo menu.
title: FMEVENT_USER_REFRESH messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 16f75f562149b50237a6b41bf2023d1f694741e3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841262"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="2a9bc-104">MESSAGGIO DI \_ AGGIORNAMENTO \_ DELL'UTENTE FMEVENT</span><span class="sxs-lookup"><span data-stu-id="2a9bc-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="2a9bc-105">Inviato a una DLL di estensione quando l'utente sceglie il **comando Aggiorna** dal menu **Visualizza** in File Manager.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="2a9bc-106">L'estensione può usare questa notifica per aggiornare il relativo menu.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a9bc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a9bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a9bc-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a9bc-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a9bc-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a9bc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a9bc-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a9bc-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a9bc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a9bc-112">Return value</span></span>

<span data-ttu-id="2a9bc-113">Una DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="2a9bc-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9bc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a9bc-114">Requirements</span></span>



| <span data-ttu-id="2a9bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9bc-115">Requirement</span></span> | <span data-ttu-id="2a9bc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2a9bc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9bc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a9bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9bc-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a9bc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2a9bc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a9bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9bc-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a9bc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2a9bc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a9bc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a9bc-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bc-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a9bc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a9bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9bc-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="2a9bc-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




