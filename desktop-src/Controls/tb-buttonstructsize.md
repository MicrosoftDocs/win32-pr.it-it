---
title: Messaggio TB_BUTTONSTRUCTSIZE (COMmctrl. h)
description: Specifica la dimensione della struttura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Controlli di Windows Message TB_BUTTONSTRUCTSIZE
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048771"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="df30a-104">TB \_ BUTTONSTRUCTSIZE messaggio</span><span class="sxs-lookup"><span data-stu-id="df30a-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="df30a-105">Specifica la dimensione della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="df30a-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="df30a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df30a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df30a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df30a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df30a-108">Dimensione, in byte, della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="df30a-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="df30a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df30a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df30a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="df30a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df30a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df30a-111">Return value</span></span>

<span data-ttu-id="df30a-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="df30a-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df30a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="df30a-113">Remarks</span></span>

<span data-ttu-id="df30a-114">Il sistema utilizza la dimensione per determinare quale versione della libreria di collegamento dinamico (DLL) del controllo comune viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="df30a-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="df30a-115">Se un'applicazione usa la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare la barra degli strumenti, l'applicazione deve inviare questo messaggio alla barra degli strumenti prima di inviare il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) o [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="df30a-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="df30a-116">La funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) invia automaticamente **TB \_ BUTTONSTRUCTSIZE** e le dimensioni della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) sono un parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="df30a-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="df30a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df30a-117">Requirements</span></span>



| <span data-ttu-id="df30a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df30a-118">Requirement</span></span> | <span data-ttu-id="df30a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="df30a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df30a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df30a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df30a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df30a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df30a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df30a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df30a-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df30a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df30a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df30a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="df30a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df30a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

