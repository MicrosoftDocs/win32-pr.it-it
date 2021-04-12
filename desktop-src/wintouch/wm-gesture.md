---
title: Messaggio WM_GESTURE (winuser. h)
description: Passa informazioni su un movimento.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE messaggio Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400764"
---
# <a name="wm_gesture-message"></a><span data-ttu-id="1d283-104">\_Messaggio di movimento WM</span><span class="sxs-lookup"><span data-stu-id="1d283-104">WM\_GESTURE message</span></span>

<span data-ttu-id="1d283-105">Passa informazioni su un movimento.</span><span class="sxs-lookup"><span data-stu-id="1d283-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d283-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d283-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d283-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d283-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d283-108">Fornisce informazioni che identificano il comando movimento e i valori di argomento specifici del movimento.</span><span class="sxs-lookup"><span data-stu-id="1d283-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="1d283-109">Queste informazioni sono le stesse informazioni passate nel membro **ullArguments** della struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .</span><span class="sxs-lookup"><span data-stu-id="1d283-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d283-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d283-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d283-111">Fornisce un handle per le informazioni che identificano il comando movimento e i valori di argomento specifici del movimento.</span><span class="sxs-lookup"><span data-stu-id="1d283-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="1d283-112">Queste informazioni vengono recuperate chiamando [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span><span class="sxs-lookup"><span data-stu-id="1d283-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d283-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d283-113">Return value</span></span>

<span data-ttu-id="1d283-114">Se un'applicazione elabora il messaggio, deve restituire 0.</span><span class="sxs-lookup"><span data-stu-id="1d283-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="1d283-115">Se l'applicazione non elabora il messaggio, deve chiamare [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="1d283-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="1d283-116">Questa operazione causerà la perdita di memoria da parte dell'applicazione perché l'handle di input tocco non verrà chiuso e la memoria del processo associata non verrà liberata.</span><span class="sxs-lookup"><span data-stu-id="1d283-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d283-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d283-117">Remarks</span></span>

<span data-ttu-id="1d283-118">Nella tabella seguente sono elencati i comandi di movimento supportati.</span><span class="sxs-lookup"><span data-stu-id="1d283-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="1d283-119">ID movimento</span><span class="sxs-lookup"><span data-stu-id="1d283-119">Gesture ID</span></span>            | <span data-ttu-id="1d283-120">Valore (*dwID*)</span><span class="sxs-lookup"><span data-stu-id="1d283-120">Value (*dwID*)</span></span> | <span data-ttu-id="1d283-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d283-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d283-122">**\_inizio GID**</span><span class="sxs-lookup"><span data-stu-id="1d283-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="1d283-123">1</span><span class="sxs-lookup"><span data-stu-id="1d283-123">1</span></span>              | <span data-ttu-id="1d283-124">Indica l'inizio di un movimento generico.</span><span class="sxs-lookup"><span data-stu-id="1d283-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="1d283-125">**\_fine GID**</span><span class="sxs-lookup"><span data-stu-id="1d283-125">**GID\_END**</span></span>          | <span data-ttu-id="1d283-126">2</span><span class="sxs-lookup"><span data-stu-id="1d283-126">2</span></span>              | <span data-ttu-id="1d283-127">Indica un'entità finale di movimento generica.</span><span class="sxs-lookup"><span data-stu-id="1d283-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="1d283-128">**\_Zoom GID**</span><span class="sxs-lookup"><span data-stu-id="1d283-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="1d283-129">3</span><span class="sxs-lookup"><span data-stu-id="1d283-129">3</span></span>              | <span data-ttu-id="1d283-130">Indica l'inizio dello zoom, lo spostamento dello zoom o l'arresto dello zoom.</span><span class="sxs-lookup"><span data-stu-id="1d283-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="1d283-131">Il primo messaggio di comando **\_ Zoom GID** avvia uno zoom ma non provoca alcuno zoom.</span><span class="sxs-lookup"><span data-stu-id="1d283-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="1d283-132">Il secondo comando di **\_ Zoom GID** attiva uno zoom rispetto allo stato contenuto nel primo **\_ Zoom GID**.</span><span class="sxs-lookup"><span data-stu-id="1d283-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="1d283-133">**Pan di GID \_**</span><span class="sxs-lookup"><span data-stu-id="1d283-133">**GID\_PAN**</span></span>          | <span data-ttu-id="1d283-134">4</span><span class="sxs-lookup"><span data-stu-id="1d283-134">4</span></span>              | <span data-ttu-id="1d283-135">Indica la panoramica dello spostamento o della panoramica.</span><span class="sxs-lookup"><span data-stu-id="1d283-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="1d283-136">Il primo comando per la **\_ Panoramica di GID** indica una panoramica di avvio ma non esegue alcuna panoramica.</span><span class="sxs-lookup"><span data-stu-id="1d283-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="1d283-137">Con il secondo messaggio del comando della **\_ Panoramica di GID** , l'applicazione inizierà la panoramica.</span><span class="sxs-lookup"><span data-stu-id="1d283-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="1d283-138">**GID \_ ruotato**</span><span class="sxs-lookup"><span data-stu-id="1d283-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="1d283-139">5</span><span class="sxs-lookup"><span data-stu-id="1d283-139">5</span></span>              | <span data-ttu-id="1d283-140">Indica l'avvio della rotazione o della rotazione.</span><span class="sxs-lookup"><span data-stu-id="1d283-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="1d283-141">Il primo messaggio di comando per la **\_ rotazione GID** indica uno spostamento o una rotazione avviata, ma non viene ruotata.</span><span class="sxs-lookup"><span data-stu-id="1d283-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="1d283-142">Il secondo messaggio di comando di rotazione **GID \_** attiverà un'operazione di rotazione relativa allo stato contenuto nella **prima \_ rotazione del GID**.</span><span class="sxs-lookup"><span data-stu-id="1d283-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="1d283-143">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="1d283-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="1d283-144">6</span><span class="sxs-lookup"><span data-stu-id="1d283-144">6</span></span>              | <span data-ttu-id="1d283-145">Indica il gesto di tocco a due dita.</span><span class="sxs-lookup"><span data-stu-id="1d283-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="1d283-146">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="1d283-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="1d283-147">7</span><span class="sxs-lookup"><span data-stu-id="1d283-147">7</span></span>              | <span data-ttu-id="1d283-148">Indica il gesto da premere e toccare.</span><span class="sxs-lookup"><span data-stu-id="1d283-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="1d283-149">Per abilitare il supporto legacy, è necessario che i messaggi con i comandi dei movimenti **\_ Begin** e **GID \_ end** si inoltrino usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="1d283-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="1d283-150">La tabella seguente indica gli argomenti del movimento passati nei parametri *lParam* e *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1d283-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="1d283-151">ID movimento</span><span class="sxs-lookup"><span data-stu-id="1d283-151">Gesture ID</span></span>            | <span data-ttu-id="1d283-152">Movimento</span><span class="sxs-lookup"><span data-stu-id="1d283-152">Gesture</span></span>        | <span data-ttu-id="1d283-153">*ullArgument*</span><span class="sxs-lookup"><span data-stu-id="1d283-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="1d283-154">*ptsLocation* nella struttura [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)</span><span class="sxs-lookup"><span data-stu-id="1d283-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d283-155">**\_Zoom GID**</span><span class="sxs-lookup"><span data-stu-id="1d283-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="1d283-156">Zoom avanti/indietro</span><span class="sxs-lookup"><span data-stu-id="1d283-156">Zoom In/Out</span></span>    | <span data-ttu-id="1d283-157">Indica la distanza tra i due punti.</span><span class="sxs-lookup"><span data-stu-id="1d283-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="1d283-158">Indica il centro dello zoom.</span><span class="sxs-lookup"><span data-stu-id="1d283-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="1d283-159">**Pan di GID \_**</span><span class="sxs-lookup"><span data-stu-id="1d283-159">**GID\_PAN**</span></span>          | <span data-ttu-id="1d283-160">Dettaglio</span><span class="sxs-lookup"><span data-stu-id="1d283-160">Pan</span></span>            | <span data-ttu-id="1d283-161">Indica la distanza tra i due punti.</span><span class="sxs-lookup"><span data-stu-id="1d283-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="1d283-162">Indica la posizione corrente del Pan.</span><span class="sxs-lookup"><span data-stu-id="1d283-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="1d283-163">**GID \_ ruotato**</span><span class="sxs-lookup"><span data-stu-id="1d283-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="1d283-164">Rotazione (pivot)</span><span class="sxs-lookup"><span data-stu-id="1d283-164">Rotate (pivot)</span></span> | <span data-ttu-id="1d283-165">Indica l'angolo di rotazione se il **flag \_ Begin di GF** è impostato.</span><span class="sxs-lookup"><span data-stu-id="1d283-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="1d283-166">In caso contrario, si tratta della modifica dell'angolo dall'avvio della rotazione.</span><span class="sxs-lookup"><span data-stu-id="1d283-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="1d283-167">Questo oggetto è firmato per indicare la direzione della rotazione.</span><span class="sxs-lookup"><span data-stu-id="1d283-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="1d283-168">Utilizzare l'angolo di [**\_ rotazione GID \_ \_ dall' \_ argomento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e l' [**\_ \_ angolo di rotazione GID a macro \_ \_ argomento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) per ottenere e impostare il valore dell'angolo.</span><span class="sxs-lookup"><span data-stu-id="1d283-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="1d283-169">Indica il centro della rotazione che rappresenta il punto fisso in cui viene ruotato l'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d283-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="1d283-170">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="1d283-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="1d283-171">Tocco con due dita</span><span class="sxs-lookup"><span data-stu-id="1d283-171">Two-finger Tap</span></span> | <span data-ttu-id="1d283-172">Indica la distanza tra le due dita.</span><span class="sxs-lookup"><span data-stu-id="1d283-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="1d283-173">Indica il centro delle due dita.</span><span class="sxs-lookup"><span data-stu-id="1d283-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="1d283-174">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="1d283-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="1d283-175">Premere e toccare</span><span class="sxs-lookup"><span data-stu-id="1d283-175">Press and Tap</span></span>  | <span data-ttu-id="1d283-176">Indica il delta tra il primo dito e il secondo dito.</span><span class="sxs-lookup"><span data-stu-id="1d283-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="1d283-177">Questo valore viene archiviato nei 32 bit inferiori di *ullArgument* in una struttura **Point** .</span><span class="sxs-lookup"><span data-stu-id="1d283-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="1d283-178">Indica la posizione in cui si arresta il primo dito.</span><span class="sxs-lookup"><span data-stu-id="1d283-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="1d283-179">Tutte le distanze e le posizioni vengono fornite nelle coordinate dello schermo fisico.</span><span class="sxs-lookup"><span data-stu-id="1d283-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d283-180">I parametri *dwID* e *ullArgument* devono essere considerati solo come allegati ai \_ \* comandi GID e non devono essere modificati dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1d283-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1d283-181">Esempio</span><span class="sxs-lookup"><span data-stu-id="1d283-181">Examples</span></span>

<span data-ttu-id="1d283-182">Nel codice seguente viene illustrato come ottenere informazioni specifiche del movimento associate a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="1d283-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="1d283-183">È necessario inviare sempre messaggi non gestiti a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) e chiudere l'handle di input del movimento per i messaggi gestiti con una chiamata a [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span><span class="sxs-lookup"><span data-stu-id="1d283-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="1d283-184">In questo esempio, il comportamento predefinito del gestore movimenti verrà eliminato perché l'handle TOUCHINPUT viene chiuso in ogni case di movimento.</span><span class="sxs-lookup"><span data-stu-id="1d283-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="1d283-185">Se i case nel codice riportato in precedenza sono stati rimossi per i messaggi non gestiti, il gestore movimenti predefinito elaborerà i messaggi eseguendo l'invio a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) nel caso predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d283-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a><span data-ttu-id="1d283-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d283-186">Requirements</span></span>



| <span data-ttu-id="1d283-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d283-187">Requirement</span></span> | <span data-ttu-id="1d283-188">Valore</span><span class="sxs-lookup"><span data-stu-id="1d283-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d283-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d283-189">Minimum supported client</span></span><br/> | <span data-ttu-id="1d283-190">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1d283-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="1d283-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d283-191">Minimum supported server</span></span><br/> | <span data-ttu-id="1d283-192">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d283-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="1d283-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d283-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d283-194"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d283-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d283-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d283-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d283-196">Notifications</span><span class="sxs-lookup"><span data-stu-id="1d283-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="1d283-197">Guida alla programmazione di movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="1d283-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

