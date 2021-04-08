---
title: Codice di notifica BN_PAINT (winuser. h)
description: Inviato quando un pulsante deve essere disegnato.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- Controlli di Windows per il codice di notifica BN_PAINT
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047870"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="8ceec-104">\_Codice di notifica della vernice BN</span><span class="sxs-lookup"><span data-stu-id="8ceec-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="8ceec-105">Inviato quando un pulsante deve essere disegnato.</span><span class="sxs-lookup"><span data-stu-id="8ceec-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="8ceec-106">Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0.</span><span class="sxs-lookup"><span data-stu-id="8ceec-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="8ceec-107">Le applicazioni devono utilizzare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.</span><span class="sxs-lookup"><span data-stu-id="8ceec-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="8ceec-108">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8ceec-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8ceec-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ceec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ceec-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ceec-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ceec-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="8ceec-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="8ceec-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="8ceec-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8ceec-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ceec-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ceec-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="8ceec-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ceec-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ceec-115">Requirements</span></span>



| <span data-ttu-id="8ceec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ceec-116">Requirement</span></span> | <span data-ttu-id="8ceec-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8ceec-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ceec-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ceec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ceec-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ceec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ceec-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ceec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ceec-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ceec-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ceec-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ceec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ceec-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ceec-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

