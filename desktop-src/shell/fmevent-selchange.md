---
description: Inviato a una DLL di estensione quando l'utente seleziona un nome file nella finestra della directory di File Manager o nella finestra Risultati ricerca.
title: FMEVENT_SELCHANGE messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: e9aa647434aab5a483626757179a7b23b3372a02
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842262"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="1f655-103">Messaggio FMEVENT \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f655-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="1f655-104">Inviato a una DLL di estensione quando l'utente seleziona un nome file nella finestra della directory di File Manager o nella finestra Risultati ricerca.</span><span class="sxs-lookup"><span data-stu-id="1f655-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f655-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f655-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f655-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f655-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1f655-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1f655-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1f655-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f655-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1f655-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1f655-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f655-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f655-110">Return value</span></span>

<span data-ttu-id="1f655-111">Una DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f655-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f655-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f655-112">Remarks</span></span>

<span data-ttu-id="1f655-113">Le modifiche nella parte dell'albero della finestra della directory non generano questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f655-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="1f655-114">Poiché l'utente può modificare la selezione più volte, la DLL di estensione deve restituire prontamente dopo l'elaborazione del messaggio per evitare di rallentare il processo di selezione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1f655-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f655-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f655-115">Requirements</span></span>



| <span data-ttu-id="1f655-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f655-116">Requirement</span></span> | <span data-ttu-id="1f655-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1f655-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f655-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f655-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f655-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f655-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1f655-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f655-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f655-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f655-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f655-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f655-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f655-123"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="1f655-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f655-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f655-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f655-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="1f655-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




