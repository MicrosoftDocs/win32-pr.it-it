---
title: Creazione di controlli comuni
description: In questo argomento viene descritto come creare una finestra che appartiene a una classe della finestra definita nella libreria di controlli comuni Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963567"
---
# <a name="creating-common-controls"></a><span data-ttu-id="8a012-103">Creazione di controlli comuni</span><span class="sxs-lookup"><span data-stu-id="8a012-103">Creating Common Controls</span></span>

<span data-ttu-id="8a012-104">In questo argomento viene descritto come creare una finestra che appartiene a una classe della finestra definita nella libreria di controlli comuni Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="8a012-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="8a012-105">La maggior parte dei controlli comuni appartiene a una classe della finestra definita nella DLL del controllo comune.</span><span class="sxs-lookup"><span data-stu-id="8a012-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="8a012-106">La classe della finestra e la corrispondente routine della finestra definiscono le proprietà, l'aspetto e il comportamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="8a012-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="8a012-107">Per assicurarsi che la DLL del controllo comune sia caricata, includere la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a012-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="8a012-108">È possibile creare un controllo comune specificando il nome della classe della finestra quando si chiama la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o specificando il nome della classe appropriato in un modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8a012-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="8a012-109">Ogni tipo di controllo comune ha un set di stili di controllo che è possibile usare per variare l'aspetto e il comportamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="8a012-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="8a012-110">La libreria di controlli comuni include anche un set di stili di controllo che si applicano a due o più tipi di controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="8a012-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="8a012-111">Gli stili di controllo comuni sono descritti nella sezione [stili](common-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8a012-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a012-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a012-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a012-113">Informazioni sui controlli comuni</span><span class="sxs-lookup"><span data-stu-id="8a012-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 