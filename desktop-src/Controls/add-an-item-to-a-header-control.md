---
title: Come aggiungere un elemento a un controllo Header
description: In questo argomento viene illustrato come aggiungere un elemento a un controllo intestazione.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963585"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="4d939-103">Come aggiungere un elemento a un controllo Header</span><span class="sxs-lookup"><span data-stu-id="4d939-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="4d939-104">In questo argomento viene illustrato come aggiungere un elemento a un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="4d939-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="4d939-105">Un controllo intestazione contiene in genere diversi elementi di intestazione che definiscono le colonne del controllo.</span><span class="sxs-lookup"><span data-stu-id="4d939-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="4d939-106">È possibile aggiungere un elemento a un controllo Header inviando il messaggio [**HDM \_ INSERTITEM**](hdm-insertitem.md) al controllo.</span><span class="sxs-lookup"><span data-stu-id="4d939-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4d939-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="4d939-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4d939-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="4d939-108">Technologies</span></span>

-   [<span data-ttu-id="4d939-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="4d939-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4d939-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4d939-110">Prerequisites</span></span>

-   <span data-ttu-id="4d939-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="4d939-111">C/C++</span></span>
-   <span data-ttu-id="4d939-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="4d939-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4d939-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4d939-113">Instructions</span></span>


<span data-ttu-id="4d939-114">Utilizzare il messaggio [**HDM \_ INSERTITEM**](hdm-insertitem.md) per aggiungere un elemento al controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="4d939-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="4d939-115">Il messaggio deve includere l'indirizzo di una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="4d939-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="4d939-116">Questa struttura definisce le proprietà dell'elemento di intestazione, che può includere una stringa, un'immagine bitmap, una dimensione iniziale e un valore a 32 bit definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d939-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="4d939-117">Nell'esempio seguente viene illustrato come utilizzare il messaggio [**\_ INSERTITEM HDM**](hdm-insertitem.md) e la struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) per aggiungere un elemento a un controllo Header.</span><span class="sxs-lookup"><span data-stu-id="4d939-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="4d939-118">Il nuovo elemento è costituito da una stringa giustificata a sinistra all'interno del rettangolo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4d939-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="4d939-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d939-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d939-120">Informazioni sui controlli intestazione</span><span class="sxs-lookup"><span data-stu-id="4d939-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="4d939-121">Riferimento al controllo intestazione</span><span class="sxs-lookup"><span data-stu-id="4d939-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4d939-122">Uso di controlli Header</span><span class="sxs-lookup"><span data-stu-id="4d939-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




