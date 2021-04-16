---
description: Usare i controlli Windows standard, laddove possibile, perché sono completamente compatibili con le linee guida di Microsoft Active Accessibility. Sono inclusi i controlli forniti da Windows (User32.dll) e dalla libreria di controlli comuni di Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Utilizzo di controlli Windows standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343286"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="2c67d-104">Utilizzo di controlli Windows standard</span><span class="sxs-lookup"><span data-stu-id="2c67d-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="2c67d-105">Usare i controlli Windows standard, laddove possibile, perché sono completamente compatibili con le linee guida di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="2c67d-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="2c67d-106">Sono inclusi i controlli forniti da Windows (User32.dll) e dalla libreria di controlli comuni di Windows (Comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="2c67d-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="2c67d-107">Ogni controllo Windows standard è una finestra separata di una classe specifica, quindi l'assistenza per l'accessibilità riceve una notifica quando lo stato attivo si sposta su un nuovo controllo.</span><span class="sxs-lookup"><span data-stu-id="2c67d-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="2c67d-108">Gli aiuti possono determinare la classe della finestra controlli e tutti i messaggi aggiuntivi che può inviare per eseguire query o modificare lo stato dei controlli.</span><span class="sxs-lookup"><span data-stu-id="2c67d-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="2c67d-109">L'assistenza può inoltre identificare tutti i controlli figlio contenuti in una finestra padre e identificare l'elemento padre di qualsiasi controllo.</span><span class="sxs-lookup"><span data-stu-id="2c67d-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="2c67d-110">Alcuni controlli comuni sono estremamente flessibili e spesso possono sostituire i controlli personalizzati meno accessibili e quelli creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="2c67d-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="2c67d-111">Una visualizzazione elenco, ad esempio, può sostituire una casella di riepilogo creata dal proprietario per visualizzare una casella di controllo accanto a ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="2c67d-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="2c67d-112">Come altro esempio, il controllo pulsante avanzato può visualizzare sia immagini che testo.</span><span class="sxs-lookup"><span data-stu-id="2c67d-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="2c67d-113">In precedenza, era necessario usare un controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2c67d-113">Previously, this required the use of a custom control.</span></span>

 

 



