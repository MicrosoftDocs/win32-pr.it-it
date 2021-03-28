---
description: Notifica a un AppBar che l'utente ha selezionato il comando Cascade, affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.
title: Messaggio ABN_WINDOWARRANGE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525422"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="f9a94-103">\_Messaggio WINDOWARRANGE di ABN</span><span class="sxs-lookup"><span data-stu-id="f9a94-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="f9a94-104">Notifica a un AppBar che l'utente ha selezionato il comando Cascade, affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f9a94-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f9a94-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9a94-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a94-106">*fBeginning*</span><span class="sxs-lookup"><span data-stu-id="f9a94-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a94-107">Flag che specifica se l'operazione Cascade o Tile è iniziata.</span><span class="sxs-lookup"><span data-stu-id="f9a94-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="f9a94-108">Questo parametro è **true** se l'operazione è iniziata e le finestre non sono ancora state spostate.</span><span class="sxs-lookup"><span data-stu-id="f9a94-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="f9a94-109">È **false** se l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f9a94-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a94-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9a94-110">Return value</span></span>

<span data-ttu-id="f9a94-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f9a94-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9a94-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9a94-112">Remarks</span></span>

<span data-ttu-id="f9a94-113">Il sistema invia questo messaggio di notifica due volte prima con *lParam* impostato su **true** e quindi con *lParam* impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="f9a94-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="f9a94-114">La prima notifica viene inviata prima che le finestre siano a cascata o affiancate, mentre la seconda viene inviata dopo l'esecuzione dell'operazione Cascade o Tile.</span><span class="sxs-lookup"><span data-stu-id="f9a94-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a94-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9a94-115">Requirements</span></span>



| <span data-ttu-id="f9a94-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9a94-116">Requirement</span></span> | <span data-ttu-id="f9a94-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a94-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a94-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9a94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a94-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9a94-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9a94-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9a94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a94-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f9a94-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9a94-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9a94-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9a94-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a94-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




