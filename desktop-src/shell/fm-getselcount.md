---
description: Inviato da un'estensione di File Manager per recuperare un conteggio dei file selezionati nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).
title: FM_GETSELCOUNT messaggio (Wfext.h)
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
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842372"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="d638b-103">Messaggio DI FM \_ GETSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="d638b-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="d638b-104">Inviato da un'estensione di File Manager per recuperare un conteggio dei file selezionati nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).</span><span class="sxs-lookup"><span data-stu-id="d638b-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="d638b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d638b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d638b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d638b-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d638b-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d638b-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d638b-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d638b-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d638b-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d638b-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d638b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d638b-110">Return value</span></span>

<span data-ttu-id="d638b-111">Restituisce il numero di file selezionati.</span><span class="sxs-lookup"><span data-stu-id="d638b-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="d638b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d638b-112">Requirements</span></span>



| <span data-ttu-id="d638b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d638b-113">Requirement</span></span> | <span data-ttu-id="d638b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d638b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d638b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d638b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d638b-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d638b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d638b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d638b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d638b-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d638b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d638b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d638b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d638b-120"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="d638b-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d638b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d638b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d638b-122">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="d638b-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="d638b-123">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="d638b-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="d638b-124">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="d638b-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




