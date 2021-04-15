---
title: Come implementare le descrizioni comandi per le icone della barra di stato
description: Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato consiste nell'implementare una descrizione comando. La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474398"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="88b04-104">Come implementare le descrizioni comandi per le icone della barra di stato</span><span class="sxs-lookup"><span data-stu-id="88b04-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="88b04-105">Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato consiste nell'implementare una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="88b04-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="88b04-106">La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="88b04-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="88b04-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="88b04-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="88b04-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="88b04-108">Technologies</span></span>

-   [<span data-ttu-id="88b04-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="88b04-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="88b04-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="88b04-110">Prerequisites</span></span>

-   <span data-ttu-id="88b04-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="88b04-111">C/C++</span></span>
-   <span data-ttu-id="88b04-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="88b04-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="88b04-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="88b04-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="88b04-114">Implementa descrizioni comandi per le icone della barra di stato</span><span class="sxs-lookup"><span data-stu-id="88b04-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="88b04-115">Il frammento di codice seguente illustra come aggiungere una descrizione comando Balloon a un'icona della barra di stato.</span><span class="sxs-lookup"><span data-stu-id="88b04-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="88b04-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="88b04-116">Remarks</span></span>

<span data-ttu-id="88b04-117">Per una descrizione dettagliata della barra di stato, vedere [la barra delle applicazioni](/windows/desktop/shell/taskbar).</span><span class="sxs-lookup"><span data-stu-id="88b04-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="88b04-118">Per visualizzare una descrizione comando a fumetti, è necessario impostare il \_ flag NSE info nella struttura [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) e usare i membri **szInfo** e **uTimeout** per specificare il testo della descrizione comando e la durata del timeout.</span><span class="sxs-lookup"><span data-stu-id="88b04-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88b04-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88b04-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88b04-120">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="88b04-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 