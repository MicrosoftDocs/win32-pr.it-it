---
description: Inviato alla finestra proprietaria di un controllo o di una voce di menu quando viene creato il controllo o il menu.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Messaggio DFM_WM_MEASUREITEM (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401617"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="fcb61-103">DFM \_ WM \_ MeasureItem messaggio</span><span class="sxs-lookup"><span data-stu-id="fcb61-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="fcb61-104">Inviato alla finestra proprietaria di un controllo o di una voce di menu quando viene creato il controllo o il menu.</span><span class="sxs-lookup"><span data-stu-id="fcb61-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="fcb61-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcb61-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb61-106">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcb61-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcb61-107">Valore del membro **CtlID** della struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lpMeasureItem* .</span><span class="sxs-lookup"><span data-stu-id="fcb61-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="fcb61-108">Questo valore identifica il controllo che ha inviato il messaggio **DFM \_ WM \_ MeasureItem** .</span><span class="sxs-lookup"><span data-stu-id="fcb61-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="fcb61-109">*lpMeasureItem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fcb61-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcb61-110">Puntatore a una struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che contiene le dimensioni del controllo creato dal proprietario o della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="fcb61-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcb61-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcb61-111">Remarks</span></span>

<span data-ttu-id="fcb61-112">Quando la finestra proprietaria riceve il messaggio **DFM \_ WM \_ MeasureItem** , il proprietario compila la struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lpMeasureItem* del messaggio e restituisce; in questo modo si informa il sistema delle dimensioni del controllo.</span><span class="sxs-lookup"><span data-stu-id="fcb61-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb61-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcb61-113">Requirements</span></span>



| <span data-ttu-id="fcb61-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb61-114">Requirement</span></span> | <span data-ttu-id="fcb61-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fcb61-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb61-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcb61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb61-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcb61-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fcb61-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcb61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb61-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fcb61-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fcb61-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcb61-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcb61-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcb61-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
