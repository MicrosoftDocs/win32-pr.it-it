---
description: Inviato da un'estensione di file Manager per fare in modo che file Manager ridisegni la finestra attiva o tutte le finestre.
title: Messaggio FM_REFRESH_WINDOWS (Wfext. h)
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
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225800"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="e8151-103">\_Messaggio di \_ Windows Refresh Refresh</span><span class="sxs-lookup"><span data-stu-id="e8151-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="e8151-104">Inviato da un'estensione di file Manager per fare in modo che file Manager ridisegni la finestra attiva o tutte le finestre.</span><span class="sxs-lookup"><span data-stu-id="e8151-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8151-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8151-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8151-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="e8151-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="e8151-107">Valore che indica se Gestione file ridisegna la finestra attiva o tutte le finestre.</span><span class="sxs-lookup"><span data-stu-id="e8151-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="e8151-108">Se questo parametro è **true**, gestione file ridisegna tutte le relative finestre.</span><span class="sxs-lookup"><span data-stu-id="e8151-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="e8151-109">In caso contrario, file Manager ridisegna solo la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="e8151-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="e8151-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8151-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8151-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e8151-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8151-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8151-112">Return value</span></span>

<span data-ttu-id="e8151-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e8151-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8151-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8151-114">Remarks</span></span>

<span data-ttu-id="e8151-115">Le modifiche del file System provocate da un'estensione vengono rilevate automaticamente da file Manager.</span><span class="sxs-lookup"><span data-stu-id="e8151-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="e8151-116">Un'estensione deve utilizzare questo messaggio solo nelle situazioni in cui le connessioni alle unità vengono effettuate o annullate.</span><span class="sxs-lookup"><span data-stu-id="e8151-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8151-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8151-117">Requirements</span></span>



| <span data-ttu-id="e8151-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8151-118">Requirement</span></span> | <span data-ttu-id="e8151-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e8151-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8151-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8151-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8151-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8151-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e8151-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8151-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8151-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8151-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8151-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8151-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8151-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8151-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8151-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8151-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8151-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="e8151-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




