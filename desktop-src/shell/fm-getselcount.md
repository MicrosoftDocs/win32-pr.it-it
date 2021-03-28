---
description: Inviato da un'estensione di file Manager per recuperare il conteggio dei file selezionati nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Messaggio FM_GETSELCOUNT (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: aac7d08de3785bb02c31dabc1ef7a25fea0d5b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993701"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="75b09-103">\_Messaggio GETSELCOUNT FM</span><span class="sxs-lookup"><span data-stu-id="75b09-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="75b09-104">Inviato da un'estensione di file Manager per recuperare il conteggio dei file selezionati nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).</span><span class="sxs-lookup"><span data-stu-id="75b09-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="75b09-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="75b09-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b09-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75b09-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="75b09-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="75b09-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="75b09-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75b09-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="75b09-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="75b09-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b09-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75b09-110">Return value</span></span>

<span data-ttu-id="75b09-111">Restituisce il numero di file selezionati.</span><span class="sxs-lookup"><span data-stu-id="75b09-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b09-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75b09-112">Requirements</span></span>



| <span data-ttu-id="75b09-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b09-113">Requirement</span></span> | <span data-ttu-id="75b09-114">Valore</span><span class="sxs-lookup"><span data-stu-id="75b09-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75b09-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b09-115">Minimum supported client</span></span><br/> | <span data-ttu-id="75b09-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75b09-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="75b09-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b09-117">Minimum supported server</span></span><br/> | <span data-ttu-id="75b09-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75b09-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="75b09-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75b09-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b09-120"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b09-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b09-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75b09-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b09-122">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="75b09-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="75b09-123">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="75b09-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="75b09-124">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="75b09-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




