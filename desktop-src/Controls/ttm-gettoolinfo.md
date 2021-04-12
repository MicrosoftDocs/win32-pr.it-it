---
title: Messaggio TTM_GETTOOLINFO (COMmctrl. h)
description: Recupera le informazioni che un controllo ToolTip gestisce su uno strumento.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- Controlli di Windows Message TTM_GETTOOLINFO
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119806"
---
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="b1daf-104">\_Messaggio TTM GETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="b1daf-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="b1daf-105">Recupera le informazioni che un controllo ToolTip gestisce su uno strumento.</span><span class="sxs-lookup"><span data-stu-id="b1daf-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1daf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1daf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1daf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1daf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b1daf-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b1daf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b1daf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1daf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1daf-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b1daf-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="b1daf-111">Quando si invia il messaggio, i membri **HWND** e **UID** identificano uno strumento e il membro **cbSize** deve specificare le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="b1daf-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="b1daf-112">Quando si usa questo messaggio per recuperare il testo della descrizione comando, verificare che il membro **lpszText** della struttura **TOOLINFO** punti a un buffer valido di dimensione adquate</span><span class="sxs-lookup"><span data-stu-id="b1daf-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1daf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1daf-113">Return value</span></span>

<span data-ttu-id="b1daf-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b1daf-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1daf-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1daf-115">Remarks</span></span>

<span data-ttu-id="b1daf-116">Se il controllo ToolTip include lo strumento, la struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) riceve informazioni sullo strumento.</span><span class="sxs-lookup"><span data-stu-id="b1daf-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="b1daf-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1daf-117">Examples</span></span>

<span data-ttu-id="b1daf-118">Nell'esempio seguente viene riposizionato un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b1daf-118">The following example repositions a tooltip control.</span></span>


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a><span data-ttu-id="b1daf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1daf-119">Requirements</span></span>



| <span data-ttu-id="b1daf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1daf-120">Requirement</span></span> | <span data-ttu-id="b1daf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b1daf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1daf-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1daf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1daf-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1daf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1daf-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1daf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1daf-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1daf-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1daf-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1daf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1daf-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1daf-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b1daf-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b1daf-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b1daf-129">**TTM \_ GETTOOLINFOW** (Unicode) e **TTM \_ GETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b1daf-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





