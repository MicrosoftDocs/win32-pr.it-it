---
title: Messaggio di EM_SETUIANAME (RichEdit. h)
description: Imposta il nome di un controllo Rich Edit per l'automazione interfaccia utente (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Controlli di Windows Message EM_SETUIANAME
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964386"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="1c7cd-104">\_Messaggio SETUIANAME em</span><span class="sxs-lookup"><span data-stu-id="1c7cd-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="1c7cd-105">Imposta il nome di un controllo Rich Edit per l'automazione interfaccia utente (UIA).</span><span class="sxs-lookup"><span data-stu-id="1c7cd-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="1c7cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c7cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c7cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c7cd-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1c7cd-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1c7cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c7cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c7cd-110">Puntatore alla stringa del nome con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="1c7cd-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7cd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c7cd-111">Return value</span></span>

<span data-ttu-id="1c7cd-112">TRUE se il nome di UIA è stato impostato correttamente; in caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="1c7cd-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7cd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c7cd-113">Requirements</span></span>



| <span data-ttu-id="1c7cd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c7cd-114">Requirement</span></span> | <span data-ttu-id="1c7cd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1c7cd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7cd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c7cd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c7cd-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1c7cd-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1c7cd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c7cd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c7cd-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1c7cd-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c7cd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c7cd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c7cd-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c7cd-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





