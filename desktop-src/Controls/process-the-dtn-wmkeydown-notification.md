---
title: Come elaborare la notifica di DTN_WMKEYDOWN
description: In questo argomento viene illustrato come elaborare una \_ notifica di DTN WMKEYDOWN. La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873137"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="950aa-104">Come elaborare la notifica DTN \_ WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="950aa-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="950aa-105">In questo argomento viene illustrato come elaborare una notifica di [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="950aa-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="950aa-106">La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.</span><span class="sxs-lookup"><span data-stu-id="950aa-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="950aa-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="950aa-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="950aa-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="950aa-108">Technologies</span></span>

-   [<span data-ttu-id="950aa-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="950aa-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="950aa-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="950aa-110">Prerequisites</span></span>

-   <span data-ttu-id="950aa-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="950aa-111">C/C++</span></span>
-   <span data-ttu-id="950aa-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="950aa-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="950aa-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="950aa-113">Instructions</span></span>


<span data-ttu-id="950aa-114">I controlli di selezione data e ora (DTP) inviano il messaggio [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) per segnalare che l'utente ha digitato l'input in un campo di callback.</span><span class="sxs-lookup"><span data-stu-id="950aa-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="950aa-115">Se si desidera emulare le stesse risposte da tastiera supportate per i campi di DTP standard o fornire risposte personalizzate, l'applicazione deve includere il codice per gestire la notifica.</span><span class="sxs-lookup"><span data-stu-id="950aa-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="950aa-116">Il seguente esempio di codice C++ è una funzione definita dall'applicazione che elabora la notifica [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="950aa-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="950aa-117">**Avviso di sicurezza:** L'uso errato di **lstrcmp** può compromettere la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="950aa-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="950aa-118">Ad esempio, prima di chiamare **lstrcmp** nell'esempio di codice seguente, è necessario assicurarsi che le due stringhe abbiano terminazione null.</span><span class="sxs-lookup"><span data-stu-id="950aa-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="950aa-119">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="950aa-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="950aa-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="950aa-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="950aa-121">Uso di controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="950aa-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="950aa-122">Riferimento al controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="950aa-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="950aa-123">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="950aa-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




