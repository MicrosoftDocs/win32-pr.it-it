---
description: Inviato quando il sistema richiede a una finestra i movimenti di sistema che si desidera ricevere.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Messaggio WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879129"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="5cb25-103">\_ \_ Messaggio QUERYSYSTEMGESTURESTATUS di WM Tablet</span><span class="sxs-lookup"><span data-stu-id="5cb25-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="5cb25-104">Inviato quando il sistema richiede a una finestra i movimenti di sistema che si desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="5cb25-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="5cb25-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cb25-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb25-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cb25-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cb25-107">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5cb25-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5cb25-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cb25-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cb25-109">Valore punto che rappresenta le coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="5cb25-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cb25-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cb25-110">Remarks</span></span>

<span data-ttu-id="5cb25-111">Grazie alla gestione di questo messaggio, è possibile disabilitare dinamicamente i gesti rapidi per le aree di una finestra.</span><span class="sxs-lookup"><span data-stu-id="5cb25-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="5cb25-112">Il *lParam* può essere convertito in coordinate x e y mediante le `GET_X_LPARAM` `GET_Y_LPARAM` macro e.</span><span class="sxs-lookup"><span data-stu-id="5cb25-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="5cb25-113">Per impostazione predefinita, la finestra riceverà tutti gli eventi di movimento del sistema.</span><span class="sxs-lookup"><span data-stu-id="5cb25-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="5cb25-114">È possibile scegliere quali eventi si desidera vengano ricevuti dalla finestra e quali eventi si desidera disabilitare rispondendo al messaggio **WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS** in **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="5cb25-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="5cb25-115">Il messaggio **WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS** è definito in tpcshrd. h.</span><span class="sxs-lookup"><span data-stu-id="5cb25-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="5cb25-116">I valori per abilitare e disabilitare i movimenti del Tablet System di sistema sono definiti anche in tpcshrd. h, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5cb25-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> <span data-ttu-id="5cb25-117">La disabilitazione di pressione propagata consente di migliorare la velocità di risposta per i clic del mouse perché questa funzionalità crea un tempo di attesa per distinguere tra le due operazioni.</span><span class="sxs-lookup"><span data-stu-id="5cb25-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="5cb25-118">Prestare attenzione durante la gestione del messaggio **WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS** .</span><span class="sxs-lookup"><span data-stu-id="5cb25-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="5cb25-119">**WM \_ Il TABLET \_ QUERYSYSTEMGESTURESTATUS** viene passato utilizzando la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="5cb25-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="5cb25-120">Se si chiamano metodi su un'interfaccia COM, tale oggetto deve trovarsi all'interno dello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="5cb25-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="5cb25-121">In caso contrario, COM genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="5cb25-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="5cb25-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="5cb25-122">Examples</span></span>

<span data-ttu-id="5cb25-123">L'esempio seguente illustra come disabilitare i gesti rapidi per un'area usando WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.</span><span class="sxs-lookup"><span data-stu-id="5cb25-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



<span data-ttu-id="5cb25-124">Nell'esempio seguente viene illustrato come disabilitare diverse funzionalità di gesti rapidi per un'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="5cb25-124">The following example shows how to disable various flicks features for an entire window.</span></span>


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a><span data-ttu-id="5cb25-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cb25-125">Requirements</span></span>



| <span data-ttu-id="5cb25-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb25-126">Requirement</span></span> | <span data-ttu-id="5cb25-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5cb25-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb25-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb25-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb25-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cb25-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5cb25-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb25-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb25-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5cb25-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5cb25-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cb25-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cb25-133"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb25-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
