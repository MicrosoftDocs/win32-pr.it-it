---
title: Codice di notifica BN_UNHILITE (winuser. h)
description: Inviato quando l'evidenziazione deve essere rimossa da un pulsante.
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- Controlli di Windows per il codice di notifica BN_UNHILITE
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395901548103a7a678b4873e1fde52e259297ebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963891"
---
# <a name="bn_unhilite-notification-code"></a><span data-ttu-id="84eb0-104">\_Codice di notifica UNHILITE BN</span><span class="sxs-lookup"><span data-stu-id="84eb0-104">BN\_UNHILITE notification code</span></span>

<span data-ttu-id="84eb0-105">Inviato quando l'evidenziazione deve essere rimossa da un pulsante.</span><span class="sxs-lookup"><span data-stu-id="84eb0-105">Sent when the highlight should be removed from a button.</span></span>

> [!Note]  
> <span data-ttu-id="84eb0-106">Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0.</span><span class="sxs-lookup"><span data-stu-id="84eb0-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="84eb0-107">Le applicazioni devono utilizzare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.</span><span class="sxs-lookup"><span data-stu-id="84eb0-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="84eb0-108">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="84eb0-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNHILITE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="84eb0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="84eb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84eb0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84eb0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84eb0-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="84eb0-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="84eb0-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="84eb0-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="84eb0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84eb0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84eb0-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="84eb0-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84eb0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="84eb0-115">Remarks</span></span>

<span data-ttu-id="84eb0-116">BN \_ UNHILITE è uguale al codice di notifica non [ \_ push di BN](bn-unpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="84eb0-116">BN\_UNHILITE is the same as the [BN\_UNPUSHED](bn-unpushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84eb0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84eb0-117">Requirements</span></span>



| <span data-ttu-id="84eb0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="84eb0-118">Requirement</span></span> | <span data-ttu-id="84eb0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="84eb0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84eb0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84eb0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84eb0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84eb0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84eb0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84eb0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84eb0-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84eb0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84eb0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84eb0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84eb0-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84eb0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

