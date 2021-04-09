---
title: Come elaborare la notifica di DTN_DATETIMECHANGE
description: In questo argomento viene illustrato come elaborare la notifica delle modifiche apportate dall'utente al controllo di selezione data e ora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963603"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="dd840-103">Come elaborare la notifica DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="dd840-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="dd840-104">In questo argomento viene illustrato come elaborare la notifica delle modifiche apportate dall'utente al controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="dd840-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="dd840-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="dd840-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="dd840-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="dd840-106">Technologies</span></span>

-   [<span data-ttu-id="dd840-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="dd840-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="dd840-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="dd840-108">Prerequisites</span></span>

-   <span data-ttu-id="dd840-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="dd840-109">C/C++</span></span>
-   <span data-ttu-id="dd840-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="dd840-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="dd840-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="dd840-111">Instructions</span></span>


<span data-ttu-id="dd840-112">Un controllo DTP invia il codice di notifica [ \_ DATETIMECHANGE di DTN](dtn-datetimechange.md) ogni volta che si verifica una modifica.</span><span class="sxs-lookup"><span data-stu-id="dd840-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="dd840-113">Questa notifica, ad esempio, verrà generata quando l'utente modifica uno dei campi del controllo o, nel caso in cui il controllo sia impostato sullo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) , quando l'utente modifica lo stato della casella di controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="dd840-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="dd840-114">L'applicazione deve includere il codice per elaborare \_ i messaggi DATETIMECHANGE di DTN inviati dal controllo DTP.</span><span class="sxs-lookup"><span data-stu-id="dd840-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="dd840-115">Il seguente esempio di codice C++ è una funzione definita dall'applicazione progettata per indicare lo stato di un controllo DTP impostato sullo stile **\_ SHOWNONE DTS** .</span><span class="sxs-lookup"><span data-stu-id="dd840-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a><span data-ttu-id="dd840-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd840-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd840-117">Uso di controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dd840-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="dd840-118">Riferimento al controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dd840-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="dd840-119">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dd840-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




