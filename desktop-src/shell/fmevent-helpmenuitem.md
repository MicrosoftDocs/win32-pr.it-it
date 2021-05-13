---
description: Inviato a una procedura DLL di estensione di File Manager quando l'utente preme F1 su un menu o una voce di comando della barra degli strumenti. L'estensione deve chiamare WinHelp, con il parametro hwnd della funzione impostato sul valore del parametro hwnd dell'estensione.
title: FMEVENT_HELPMENUITEM messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842312"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="5cb89-104">Messaggio \_ HELPMENUITEM FMEVENT</span><span class="sxs-lookup"><span data-stu-id="5cb89-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="5cb89-105">Inviato a una procedura DLL di estensione di File Manager quando l'utente preme F1 su un menu o una voce di comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5cb89-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="5cb89-106">L'estensione deve [**chiamare WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), con il parametro *hwnd* della funzione impostato sul valore del parametro *hwnd* dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5cb89-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cb89-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cb89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb89-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cb89-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5cb89-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5cb89-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5cb89-110">*uItem*</span><span class="sxs-lookup"><span data-stu-id="5cb89-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="5cb89-111">Valore che identifica la voce di menu o di comando della barra degli strumenti per cui si desidera visualizzare la Guida.</span><span class="sxs-lookup"><span data-stu-id="5cb89-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="5cb89-112">La procedura di estensione usa questo valore per determinare il modo migliore per chiamare [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)</span><span class="sxs-lookup"><span data-stu-id="5cb89-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb89-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cb89-113">Return value</span></span>

<span data-ttu-id="5cb89-114">Una routine DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="5cb89-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb89-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cb89-115">Requirements</span></span>



| <span data-ttu-id="5cb89-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb89-116">Requirement</span></span> | <span data-ttu-id="5cb89-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5cb89-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb89-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb89-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5cb89-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5cb89-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb89-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5cb89-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5cb89-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cb89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cb89-123"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb89-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb89-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cb89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb89-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="5cb89-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="5cb89-126">**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="5cb89-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




