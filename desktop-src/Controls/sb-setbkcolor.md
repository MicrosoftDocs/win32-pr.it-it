---
title: Messaggio SB_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo di una barra di stato.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Controlli di Windows Message SB_SETBKCOLOR
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400827"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="a4bc1-104">\_Messaggio SETBKCOLOR SB</span><span class="sxs-lookup"><span data-stu-id="a4bc1-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="a4bc1-105">Imposta il colore di sfondo di una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="a4bc1-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4bc1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4bc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4bc1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4bc1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a4bc1-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a4bc1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a4bc1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4bc1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4bc1-110">Valore [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il nuovo colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="a4bc1-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="a4bc1-111">Specificare il \_ valore predefinito CLR per fare in modo che la barra di stato usi il colore di sfondo predefinito.</span><span class="sxs-lookup"><span data-stu-id="a4bc1-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4bc1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4bc1-112">Return value</span></span>

<span data-ttu-id="a4bc1-113">Restituisce il colore di sfondo precedente oppure il \_ valore predefinito CLR se il colore di sfondo è il colore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a4bc1-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bc1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4bc1-114">Requirements</span></span>



| <span data-ttu-id="a4bc1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4bc1-115">Requirement</span></span> | <span data-ttu-id="a4bc1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a4bc1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bc1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4bc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4bc1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4bc1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4bc1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4bc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4bc1-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4bc1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4bc1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4bc1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4bc1-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4bc1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

