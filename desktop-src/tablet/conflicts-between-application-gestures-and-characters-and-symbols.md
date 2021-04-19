---
description: Descrizione dei conflitti tra i movimenti dell'applicazione e i caratteri e i simboli.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflitti tra movimenti dell'applicazione e caratteri e simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305685"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a><span data-ttu-id="6beaa-103">Conflitti tra movimenti dell'applicazione e caratteri e simboli</span><span class="sxs-lookup"><span data-stu-id="6beaa-103">Conflicts Between Application Gestures and Characters and Symbols</span></span>

<span data-ttu-id="6beaa-104">Alcuni movimenti dell'applicazione possono entrare in conflitto con caratteri, combinazioni di caratteri, simboli, combinazioni di caratteri e simboli o parole intere scritte in un singolo tratto.</span><span class="sxs-lookup"><span data-stu-id="6beaa-104">Some application gestures may conflict with characters, combinations of characters, symbols, combinations of characters and symbols or whole words written in a single stroke.</span></span> <span data-ttu-id="6beaa-105">La maggior parte di questi conflitti viene evitata con una conoscenza approfondita del contesto in cui viene eseguito il movimento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6beaa-105">Most of these conflicts are avoided by having a detailed understanding of the context in which the application gesture is performed.</span></span>

<span data-ttu-id="6beaa-106">Ad esempio, per distinguere un gesto destro da un trattino (-) o da un carattere di sottolineatura ( \_ ), un'applicazione può filtrare in base al modo in cui il movimento si avvicina ai caratteri adiacenti, alla dimensione relativa rispetto ai caratteri o ad altre informazioni contenute in un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6beaa-106">For example, to distinguish a right gesture from a dash (-) or an underscore (\_), an application may filter for how close the gesture is to neighboring characters, the relative size as compared to characters, or other information contained in a packet.</span></span> <span data-ttu-id="6beaa-107">La tempistica del movimento dell'applicazione può anche essere un fattore determinante nella scelta tra movimenti e caratteri.</span><span class="sxs-lookup"><span data-stu-id="6beaa-107">The timing of the application gesture may also be a determining factor in deciding between gestures and characters.</span></span> <span data-ttu-id="6beaa-108">Prima di applicare un movimento di un'applicazione, è possibile che si verifichi una pausa prima di inserire i caratteri.</span><span class="sxs-lookup"><span data-stu-id="6beaa-108">There may be more of a pause before applying an application gesture than before inputting characters.</span></span> <span data-ttu-id="6beaa-109">A meno che un utente non esegua una serie di movimenti di annullamento o BACKSPACE, potrebbe anche esserci più di una pausa dopo un movimento rispetto a un carattere.</span><span class="sxs-lookup"><span data-stu-id="6beaa-109">Unless a user is performing a series of undo or backspace gestures, there may also be more of a pause after a gesture than a character.</span></span>

<span data-ttu-id="6beaa-110">Gli argomenti seguenti illustrano in dettaglio questi conflitti:</span><span class="sxs-lookup"><span data-stu-id="6beaa-110">The following topics detail these conflicts:</span></span>

-   [<span data-ttu-id="6beaa-111">Conflitti con caratteri latini e simboli</span><span class="sxs-lookup"><span data-stu-id="6beaa-111">Conflicts with Latin characters and symbols</span></span>](conflicts-with-latin-characters-and-symbols.md)
-   [<span data-ttu-id="6beaa-112">Conflitti con caratteri East-Asian</span><span class="sxs-lookup"><span data-stu-id="6beaa-112">Conflicts with East-Asian Characters</span></span>](conflicts-with-east-asian-characters.md)

 

 



