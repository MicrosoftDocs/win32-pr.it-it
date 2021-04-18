---
title: Input del mouse (introduzione a Win32 e C++)
description: Input del mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300746"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="5df0d-103">Input del mouse (introduzione a Win32 e C++)</span><span class="sxs-lookup"><span data-stu-id="5df0d-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="5df0d-104">Windows supporta i topi con un massimo di cinque pulsanti: Left, Middle e Right, oltre a due pulsanti aggiuntivi denominati XBUTTON1 e XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="5df0d-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![illustrazione che mostra i pulsanti a sinistra (1), a destra (2), a metà (3) e a XButton1 (4).](images/mouse.png)

<span data-ttu-id="5df0d-106">Per la maggior parte dei topi per Windows sono disponibili almeno i pulsanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="5df0d-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="5df0d-107">Il pulsante sinistro del mouse viene usato per puntare, selezionare, trascinare e così via.</span><span class="sxs-lookup"><span data-stu-id="5df0d-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="5df0d-108">Il pulsante destro del mouse Visualizza in genere un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5df0d-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="5df0d-109">Alcuni topi hanno una rotellina di scorrimento posizionata tra i pulsanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="5df0d-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="5df0d-110">A seconda del mouse, è possibile che la rotellina di scorrimento sia anche selezionabile, rendendola il pulsante intermedio.</span><span class="sxs-lookup"><span data-stu-id="5df0d-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="5df0d-111">I pulsanti XBUTTON1 e XBUTTON2 si trovano spesso sui lati del mouse, vicino alla base.</span><span class="sxs-lookup"><span data-stu-id="5df0d-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="5df0d-112">Questi pulsanti aggiuntivi non sono presenti in tutti i topi.</span><span class="sxs-lookup"><span data-stu-id="5df0d-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="5df0d-113">Se presente, i pulsanti XBUTTON1 e XBUTTON2 vengono spesso mappati a una funzione dell'applicazione, ad esempio la navigazione in avanti e indietro in un Web browser.</span><span class="sxs-lookup"><span data-stu-id="5df0d-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="5df0d-114">Gli utenti a sinistra spesso trovano più comodo scambiare le funzioni dei pulsanti sinistro e destro, usando il pulsante destro come puntatore, e il pulsante sinistro per visualizzare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5df0d-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="5df0d-115">Per questo motivo, nella documentazione della Guida di Windows vengono usati il pulsante dei termini *primari* e i *pulsanti secondari*, che fanno riferimento alla funzione logica anziché alla posizione fisica.</span><span class="sxs-lookup"><span data-stu-id="5df0d-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="5df0d-116">Nell'impostazione predefinita (a destra), il pulsante sinistro è il pulsante primario e quello secondario.</span><span class="sxs-lookup"><span data-stu-id="5df0d-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="5df0d-117">Tuttavia, i termini *con il pulsante destro del mouse* e il *clic sinistro* fanno riferimento a azioni logiche.</span><span class="sxs-lookup"><span data-stu-id="5df0d-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="5df0d-118">*Facendo clic con* il pulsante destro del mouse si fa clic sul pulsante principale, se il pulsante è fisicamente sul lato destro o sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="5df0d-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="5df0d-119">Indipendentemente dal modo in cui l'utente configura il mouse, Windows converte automaticamente i messaggi del mouse in modo che siano coerenti.</span><span class="sxs-lookup"><span data-stu-id="5df0d-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="5df0d-120">L'utente può scambiare i pulsanti primari e secondari al centro dell'utilizzo del programma e non influirà sul comportamento del programma.</span><span class="sxs-lookup"><span data-stu-id="5df0d-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="5df0d-121">La documentazione MSDN usa il pulsante a *destra* e il pulsante *sinistro* per indicare il pulsante *primario* e *secondario* .</span><span class="sxs-lookup"><span data-stu-id="5df0d-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="5df0d-122">Questa terminologia è coerente con i nomi dei messaggi della finestra per l'input del mouse.</span><span class="sxs-lookup"><span data-stu-id="5df0d-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="5df0d-123">È sufficiente ricordare che i pulsanti fisici sinistro e destro potrebbero essere scambiati.</span><span class="sxs-lookup"><span data-stu-id="5df0d-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="5df0d-124">Prossima</span><span class="sxs-lookup"><span data-stu-id="5df0d-124">Next</span></span>

[<span data-ttu-id="5df0d-125">Risposta ai clic del mouse</span><span class="sxs-lookup"><span data-stu-id="5df0d-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




