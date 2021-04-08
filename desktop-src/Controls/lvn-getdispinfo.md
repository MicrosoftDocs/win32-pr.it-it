---
title: Codice di notifica LVN_GETDISPINFO (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco alla relativa finestra padre. Si tratta di una richiesta per la finestra padre per fornire le informazioni necessarie per visualizzare o ordinare un elemento della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- Controlli di Windows per il codice di notifica LVN_GETDISPINFO
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744002"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="f929e-106">\_Codice di notifica GETDISPINFO di LVN</span><span class="sxs-lookup"><span data-stu-id="f929e-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="f929e-107">Inviato da un controllo di visualizzazione elenco alla relativa finestra padre.</span><span class="sxs-lookup"><span data-stu-id="f929e-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="f929e-108">Si tratta di una richiesta per la finestra padre per fornire le informazioni necessarie per visualizzare o ordinare un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="f929e-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="f929e-109">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f929e-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="f929e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f929e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f929e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f929e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f929e-112">Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f929e-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="f929e-113">In input la struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenuta in questa struttura specifica il tipo di informazioni richieste e identifica l'elemento o l'elemento secondario di interesse.</span><span class="sxs-lookup"><span data-stu-id="f929e-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="f929e-114">Utilizzare la struttura **LVITEM** per restituire al controllo le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="f929e-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="f929e-115">Se il gestore di messaggi imposta il \_ flag LVIF di \_ SetItem nel membro **mask** della struttura **LVITEM** , il controllo List-View archivia le informazioni richieste e non le richiede di nuovo.</span><span class="sxs-lookup"><span data-stu-id="f929e-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f929e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f929e-116">Return value</span></span>

<span data-ttu-id="f929e-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f929e-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f929e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f929e-118">Remarks</span></span>

<span data-ttu-id="f929e-119">Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f929e-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="f929e-120">Il parametro *wParam* contiene il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="f929e-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="f929e-121">Un controllo di visualizzazione elenco Invia il codice di notifica **\_ GETDISPINFO LVN** per recuperare le informazioni sull'elemento archiviate dall'applicazione anziché dal controllo.</span><span class="sxs-lookup"><span data-stu-id="f929e-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="f929e-122">Le informazioni possono essere informazioni sul testo o sull'icona per un elemento.</span><span class="sxs-lookup"><span data-stu-id="f929e-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="f929e-123">Può anche essere informazioni sullo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f929e-123">It can also be item state information.</span></span> <span data-ttu-id="f929e-124">Per ulteriori informazioni sull'implementazione dello stato dell'elemento in base a un callback, vedere il messaggio [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f929e-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="f929e-125">Per altre informazioni sui callback di visualizzazione elenco, vedere [elementi di callback e maschera di callback](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f929e-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f929e-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="f929e-126">Examples</span></span>

<span data-ttu-id="f929e-127">Nell'esempio seguente viene illustrato il modo in cui questo codice di notifica può essere gestito per impostare il testo nelle colonne di una visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="f929e-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="f929e-128">I dati per ogni elemento sono contenuti nella struttura seguente.</span><span class="sxs-lookup"><span data-stu-id="f929e-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="f929e-129">Il codice seguente è riportato dal \_ gestore di notifiche WM nella procedura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f929e-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="f929e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f929e-130">Requirements</span></span>



| <span data-ttu-id="f929e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f929e-131">Requirement</span></span> | <span data-ttu-id="f929e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f929e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f929e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f929e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f929e-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f929e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f929e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f929e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f929e-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f929e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f929e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f929e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f929e-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f929e-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f929e-139">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f929e-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f929e-140">**LVN \_ GETDISPINFOW** (Unicode) e **LVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f929e-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f929e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f929e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f929e-142">**\_SETDISPINFO LVN**</span><span class="sxs-lookup"><span data-stu-id="f929e-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





