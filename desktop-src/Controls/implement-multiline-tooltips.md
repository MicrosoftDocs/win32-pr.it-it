---
title: Come implementare descrizioni comandi su più righe
description: Le descrizioni comando su più righe consentono di visualizzare il testo su più di una riga.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708662"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="37a42-103">Come implementare descrizioni comandi su più righe</span><span class="sxs-lookup"><span data-stu-id="37a42-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="37a42-104">Le descrizioni comando su più righe consentono di visualizzare il testo su più di una riga.</span><span class="sxs-lookup"><span data-stu-id="37a42-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="37a42-105">Sono supportati dalla [versione 4,70](common-control-versions.md) e successive dei controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="37a42-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="37a42-106">L'applicazione crea una descrizione comando su più righe inviando un messaggio [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , specificando la larghezza del rettangolo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="37a42-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="37a42-107">Il testo che supera questa larghezza va a capo alla riga successiva anziché ampliare l'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="37a42-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="37a42-108">L'altezza del rettangolo viene aumentata in base alle esigenze per contenere le righe aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="37a42-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="37a42-109">Il controllo ToolTip esegue automaticamente il wrapping delle righe, oppure è possibile usare una combinazione di ritorno a capo/avanzamento riga, \\ r \\ n, per forzare le interruzioni di riga in posizioni particolari.</span><span class="sxs-lookup"><span data-stu-id="37a42-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="37a42-110">La visualizzazione risultante è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="37a42-110">The resulting display is shown in the following illustration.</span></span>

![Screenshot di una finestra di dialogo con una descrizione comando contenente testo disposto come un paragrafo a più righe](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="37a42-112">Il buffer di testo specificato dal membro **szText** della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) può contenere solo 80 caratteri.</span><span class="sxs-lookup"><span data-stu-id="37a42-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="37a42-113">Se è necessario usare una stringa più lunga, puntare il membro **lpszText** di **NMTTDISPINFO** a un buffer contenente il testo desiderato.</span><span class="sxs-lookup"><span data-stu-id="37a42-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="37a42-114">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="37a42-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="37a42-115">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="37a42-115">Technologies</span></span>

-   [<span data-ttu-id="37a42-116">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="37a42-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="37a42-117">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="37a42-117">Prerequisites</span></span>

-   <span data-ttu-id="37a42-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="37a42-118">C/C++</span></span>
-   <span data-ttu-id="37a42-119">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="37a42-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="37a42-120">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="37a42-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="37a42-121">Implementare descrizioni comandi su più righe</span><span class="sxs-lookup"><span data-stu-id="37a42-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="37a42-122">Il frammento di codice seguente è un esempio di un semplice gestore di notifiche [ \_ GETDISPINFO TTN](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="37a42-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="37a42-123">Abilita una descrizione comando su più righe impostando il rettangolo di visualizzazione su 150 pixel.</span><span class="sxs-lookup"><span data-stu-id="37a42-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="37a42-124">Viene inserita un'interruzione di riga manuale dopo la prima parola per mostrare che le interruzioni di riga possono essere rigide e morbide.</span><span class="sxs-lookup"><span data-stu-id="37a42-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="37a42-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37a42-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a42-126">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="37a42-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




