---
title: Messaggio WM_NEXTMENU (winuser. h)
description: Inviato a un'applicazione quando viene usato il tasto freccia destra o sinistra per passare dalla barra dei menu al menu di sistema e viceversa.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- Menu del messaggio WM_NEXTMENU e altre risorse
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964970"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="75d81-104">\_Messaggio NEXTMENU WM</span><span class="sxs-lookup"><span data-stu-id="75d81-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="75d81-105">Inviato a un'applicazione quando viene usato il tasto freccia destra o sinistra per passare dalla barra dei menu al menu di sistema e viceversa.</span><span class="sxs-lookup"><span data-stu-id="75d81-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="75d81-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75d81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d81-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75d81-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75d81-108">Codice della chiave virtuale della chiave.</span><span class="sxs-lookup"><span data-stu-id="75d81-108">The virtual-key code of the key.</span></span> <span data-ttu-id="75d81-109">Vedere [**codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="75d81-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="75d81-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75d81-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75d81-111">Puntatore a una struttura [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) contenente informazioni sul menu da attivare.</span><span class="sxs-lookup"><span data-stu-id="75d81-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75d81-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="75d81-112">Remarks</span></span>

<span data-ttu-id="75d81-113">In risposta a questo messaggio, l'applicazione può specificare il menu a cui passare nel membro **hmenuNext** di [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) e la finestra per ricevere i messaggi di notifica del menu nel membro **hwndNext** della struttura **MDINEXTMENU** .</span><span class="sxs-lookup"><span data-stu-id="75d81-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="75d81-114">Per rendere effettive le modifiche, è necessario impostare entrambi i membri (inizialmente **null**).</span><span class="sxs-lookup"><span data-stu-id="75d81-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="75d81-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75d81-115">Requirements</span></span>



| <span data-ttu-id="75d81-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d81-116">Requirement</span></span> | <span data-ttu-id="75d81-117">Valore</span><span class="sxs-lookup"><span data-stu-id="75d81-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d81-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d81-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75d81-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75d81-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="75d81-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d81-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75d81-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75d81-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75d81-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75d81-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d81-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75d81-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d81-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75d81-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="75d81-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="75d81-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75d81-126">**MDINEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="75d81-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="75d81-127">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="75d81-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75d81-128">Menu</span><span class="sxs-lookup"><span data-stu-id="75d81-128">Menus</span></span>](menus.md)
</dt> </dl>

 

