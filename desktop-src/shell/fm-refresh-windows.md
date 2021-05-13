---
description: Inviato da un'estensione di File Manager per fare in modo che File Manager ridisegni la finestra attiva o tutte le finestre.
title: FM_REFRESH_WINDOWS messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842352"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="549d6-103">MESSAGGIO \_ DI WINDOWS FM REFRESH \_</span><span class="sxs-lookup"><span data-stu-id="549d6-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="549d6-104">Inviato da un'estensione di File Manager per fare in modo che File Manager ridisegni la finestra attiva o tutte le finestre.</span><span class="sxs-lookup"><span data-stu-id="549d6-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="549d6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="549d6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549d6-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="549d6-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="549d6-107">Valore che indica se File Manager ridisegna la finestra attiva o tutte le finestre.</span><span class="sxs-lookup"><span data-stu-id="549d6-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="549d6-108">Se questo parametro è **TRUE,** File Manager ridisegna tutte le finestre.</span><span class="sxs-lookup"><span data-stu-id="549d6-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="549d6-109">In caso contrario, File Manager ridisegna solo la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="549d6-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="549d6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="549d6-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="549d6-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="549d6-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549d6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="549d6-112">Return value</span></span>

<span data-ttu-id="549d6-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="549d6-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="549d6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="549d6-114">Remarks</span></span>

<span data-ttu-id="549d6-115">Le modifiche al file system causate da un'estensione vengono rilevate automaticamente da File Manager.</span><span class="sxs-lookup"><span data-stu-id="549d6-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="549d6-116">Un'estensione deve utilizzare questo messaggio solo nelle situazioni in cui le connessioni alle unità vengono effettuate o annullate.</span><span class="sxs-lookup"><span data-stu-id="549d6-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="549d6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="549d6-117">Requirements</span></span>



| <span data-ttu-id="549d6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="549d6-118">Requirement</span></span> | <span data-ttu-id="549d6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="549d6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="549d6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="549d6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="549d6-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="549d6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="549d6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="549d6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="549d6-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="549d6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="549d6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="549d6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="549d6-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="549d6-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="549d6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="549d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549d6-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="549d6-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




