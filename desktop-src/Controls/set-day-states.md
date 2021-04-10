---
title: Come impostare gli Stati del giorno
description: In questo argomento viene illustrato come impostare le informazioni sullo stato del giorno. Il controllo calendario mensile usa le informazioni sullo stato del giorno per determinare come vengono disegnati giorni specifici all'interno del controllo.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963599"
---
# <a name="how-to-set-day-states"></a><span data-ttu-id="05ced-104">Come impostare gli Stati del giorno</span><span class="sxs-lookup"><span data-stu-id="05ced-104">How to Set Day States</span></span>

<span data-ttu-id="05ced-105">In questo argomento viene illustrato come impostare le informazioni sullo stato del giorno.</span><span class="sxs-lookup"><span data-stu-id="05ced-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="05ced-106">Il controllo calendario mensile usa le informazioni sullo stato del giorno per determinare come vengono disegnati giorni specifici all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="05ced-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="05ced-107">Controlli di calendario mensile che usano gli Stati del giorno del supporto di tipo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="05ced-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="05ced-108">Le informazioni sullo stato del giorno sono espresse come tipo di dati a 32 bit, [**MONTHDAYSTATE**](monthdaystate.md).</span><span class="sxs-lookup"><span data-stu-id="05ced-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="05ced-109">Ogni bit in un bit **MONTHDAYSTATE** (da 0 a 30) specifica lo stato di un giorno in un mese.</span><span class="sxs-lookup"><span data-stu-id="05ced-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="05ced-110">Se un bit è acceso, il giorno corrispondente viene visualizzato in grassetto.</span><span class="sxs-lookup"><span data-stu-id="05ced-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="05ced-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="05ced-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="05ced-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="05ced-112">Technologies</span></span>

-   [<span data-ttu-id="05ced-113">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="05ced-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="05ced-114">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="05ced-114">Prerequisites</span></span>

-   <span data-ttu-id="05ced-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="05ced-115">C/C++</span></span>
-   <span data-ttu-id="05ced-116">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="05ced-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="05ced-117">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="05ced-117">Instructions</span></span>


<span data-ttu-id="05ced-118">Un'applicazione può impostare in modo esplicito le informazioni sullo stato del giorno inviando il messaggio [**\_ SETDAYSTATE MCM**](mcm-setdaystate.md) o usando la macro corrispondente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="05ced-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="05ced-119">Tuttavia, le informazioni sullo stato del giorno vengono in genere impostate in risposta al codice di notifica [ \_ GETDAYSTATE di MCN](mcn-getdaystate.md) , che viene inviato ogni volta che è necessario aggiornare il controllo perché, ad esempio, è stato eseguito lo scorrimento nella visualizzazione di un mese diverso.</span><span class="sxs-lookup"><span data-stu-id="05ced-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="05ced-120">Nell'esempio di codice seguente viene illustrato come elaborare il codice di notifica [ \_ GETDAYSTATE di MCN](mcn-getdaystate.md) in un gestore di messaggi di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="05ced-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="05ced-121">Elabora MCN \_ GETDAYSTATE specificando che il primo e il quindicesimo giorno di ogni mese visibile devono essere evidenziati.</span><span class="sxs-lookup"><span data-stu-id="05ced-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="05ced-122">Il membro **cDayState** della struttura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) specifica il numero di valori [**MONTHDAYSTATE**](monthdaystate.md) necessari nella matrice, a cui viene assegnata una dimensione massima arbitraria.</span><span class="sxs-lookup"><span data-stu-id="05ced-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="05ced-123">Il codice esegue quindi il ciclo per impostare i bit appropriati in ogni elemento valido della matrice, usando la macro **BOLDDAY** definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05ced-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a><span data-ttu-id="05ced-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05ced-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ced-125">Riferimento al controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="05ced-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="05ced-126">Informazioni sui controlli calendario mensile</span><span class="sxs-lookup"><span data-stu-id="05ced-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="05ced-127">Utilizzo di controlli calendario mensile</span><span class="sxs-lookup"><span data-stu-id="05ced-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 




