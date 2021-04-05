---
title: Appendice B supporto per gestione finestre di dialogo standard
description: Microsoft Active Accessibility fornisce il supporto completo per i controlli della finestra di dialogo Gestione finestre di dialogo standard (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710867"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="b4560-103">Appendice B: supporto di gestione finestre di dialogo standard</span><span class="sxs-lookup"><span data-stu-id="b4560-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="b4560-104">Microsoft Active Accessibility fornisce il supporto completo per i controlli della finestra di dialogo Gestione finestre di dialogo standard (SDM).</span><span class="sxs-lookup"><span data-stu-id="b4560-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="b4560-105">SDM è una libreria di codici Microsoft interna che fornisce alle applicazioni Microsoft un livello di indipendenza dalle differenze tra i sistemi operativi Macintosh e Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b4560-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="b4560-106">SDM viene usato principalmente per le finestre di dialogo in Microsoft Excel e Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b4560-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="b4560-107">SDM presenta problemi per gli strumenti di accessibilità perché usa implementazioni non standard delle finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b4560-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="b4560-108">Ad esempio, i pulsanti della finestra di dialogo SDM non utilizzano gli handle di finestra in modo analogo agli elementi dell'interfaccia utente standard.</span><span class="sxs-lookup"><span data-stu-id="b4560-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="b4560-109">Non è possibile inviare messaggi a pulsanti e pulsanti non inclusi nell'elenco di finestre.</span><span class="sxs-lookup"><span data-stu-id="b4560-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="b4560-110">Un'applicazione che utilizza SDM comunica con il controllo tramite un'interfaccia privata.</span><span class="sxs-lookup"><span data-stu-id="b4560-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="b4560-111">Nella figura seguente viene illustrata una finestra di dialogo di esempio di Word.</span><span class="sxs-lookup"><span data-stu-id="b4560-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="b4560-112">Sebbene sembri una normale finestra di dialogo di Windows che usa il controllo Tab, si tratta in realtà di una finestra di dialogo SDM.</span><span class="sxs-lookup"><span data-stu-id="b4560-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![screenshot della finestra di dialogo Opzioni con la scheda Visualizza selezionata](images/dialog.gif)

 

 




