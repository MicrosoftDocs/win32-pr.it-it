---
description: Notifica a un AppBar quando si è verificato un evento che può influire sulle dimensioni e la posizione di AppBar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Messaggio ABN_POSCHANGED (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977426"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="a171d-103">\_Messaggio POSCHANGED di ABN</span><span class="sxs-lookup"><span data-stu-id="a171d-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="a171d-104">Notifica a un AppBar quando si è verificato un evento che può influire sulle dimensioni e la posizione di AppBar.</span><span class="sxs-lookup"><span data-stu-id="a171d-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="a171d-105">Gli eventi includono le modifiche apportate alle dimensioni, alla posizione e allo stato di visibilità della barra delle applicazioni, nonché l'aggiunta, la rimozione o il ridimensionamento di un altro AppBar sullo stesso lato dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a171d-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="a171d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a171d-106">Parameters</span></span>

<span data-ttu-id="a171d-107">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="a171d-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a171d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a171d-108">Return value</span></span>

<span data-ttu-id="a171d-109">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a171d-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a171d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a171d-110">Remarks</span></span>

<span data-ttu-id="a171d-111">Un AppBar deve rispondere a questo messaggio di notifica inviando i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="a171d-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="a171d-112">Se la posizione è cambiata, AppBar deve chiamare la funzione [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) per spostarsi alla nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="a171d-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="a171d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a171d-113">Requirements</span></span>



| <span data-ttu-id="a171d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a171d-114">Requirement</span></span> | <span data-ttu-id="a171d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a171d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a171d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a171d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a171d-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a171d-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a171d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a171d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a171d-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a171d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a171d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a171d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a171d-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a171d-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

