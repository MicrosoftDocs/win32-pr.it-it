---
description: Un contesto di dispositivo padre consente a un'applicazione di ridurre al minimo il tempo necessario per configurare l'area di visualizzazione per una finestra.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Contesti dispositivo di visualizzazione padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978442"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="ad262-103">Contesti dispositivo di visualizzazione padre</span><span class="sxs-lookup"><span data-stu-id="ad262-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="ad262-104">Un *contesto di dispositivo padre* consente a un'applicazione di ridurre al minimo il tempo necessario per configurare l'area di visualizzazione per una finestra.</span><span class="sxs-lookup"><span data-stu-id="ad262-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="ad262-105">Un'applicazione usa in genere i contesti di dispositivo padre per velocizzare il disegno per le finestre di controllo senza richiedere un contesto di dispositivo privato o di classe.</span><span class="sxs-lookup"><span data-stu-id="ad262-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="ad262-106">Ad esempio, il sistema usa i contesti di dispositivo padre per i pulsanti di comando e di modifica.</span><span class="sxs-lookup"><span data-stu-id="ad262-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="ad262-107">I contesti di dispositivo padre sono destinati all'uso solo con le finestre figlio, mai con finestre popup o di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ad262-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="ad262-108">Un'applicazione può specificare lo \_ stile cs PARENTDC per impostare l'area di visualizzazione della finestra figlio sulla finestra padre in modo che l'elemento figlio possa disegnarlo nell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="ad262-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="ad262-109">La specifica di CS \_ PARENTDC migliora le prestazioni di un'applicazione perché non è necessario che il sistema continui a ricalcolare l'area visibile per ogni finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="ad262-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="ad262-110">I valori di attributo impostati dalla finestra padre non vengono conservati per la finestra figlio; la finestra padre, ad esempio, non può impostare il pennello per le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="ad262-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="ad262-111">L'unica proprietà conservata è l'area di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ad262-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="ad262-112">La finestra deve ritagliare il proprio output ai limiti della finestra.</span><span class="sxs-lookup"><span data-stu-id="ad262-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="ad262-113">Poiché l'area di ridimensionamento per il contesto di dispositivo padre è identica alla finestra padre, è possibile che la finestra figlio si avvicini all'intera finestra padre, ma il contesto di dispositivo padre non deve essere usato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="ad262-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="ad262-114">Il sistema ignora lo stile CS \_ PARENTDC se la finestra padre utilizza un contesto di dispositivo privato o di classe, se la finestra padre Ritaglia le finestre figlio o se la finestra figlio Ritaglia le finestre figlio o le finestre di pari livello.</span><span class="sxs-lookup"><span data-stu-id="ad262-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 



