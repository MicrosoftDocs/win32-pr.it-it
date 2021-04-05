---
title: Visualizzazione di interfacce utente modali
description: Visualizzazione di interfacce utente modali
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Plug-in di Windows Media Player, visualizzazione di finestre di dialogo e finestre di messaggio
- plug-in, visualizzazione di finestre di dialogo e finestre di messaggio
- plug-in dell'interfaccia utente, visualizzazione di finestre di dialogo e finestre di messaggio
- Plug-in dell'interfaccia utente, visualizzazione di finestre di dialogo e finestre di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714527"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="bca87-107">Visualizzazione di interfacce utente modali</span><span class="sxs-lookup"><span data-stu-id="bca87-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="bca87-108">I plug-in dell'interfaccia utente non devono visualizzare le finestre di dialogo o le finestre di messaggio modali in risposta alle chiamate al metodo da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bca87-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="bca87-109">Ad esempio, non visualizzare una finestra di messaggio dall'implementazione di **IWMPPluginUI:: create**.</span><span class="sxs-lookup"><span data-stu-id="bca87-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="bca87-110">Se è necessario visualizzare una finestra di dialogo o una finestra di messaggio da un'implementazione del metodo del plug-in dell'interfaccia utente chiamata dal lettore, è necessario attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="bca87-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="bca87-111">Registrare un nuovo messaggio della finestra usando **RegisterWindowMessage**.</span><span class="sxs-lookup"><span data-stu-id="bca87-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="bca87-112">Inviare il messaggio della finestra registrato nella finestra del plug-in dell'interfaccia utente usando **PostMessage**.</span><span class="sxs-lookup"><span data-stu-id="bca87-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="bca87-113">Visualizza la finestra di dialogo o la finestra di messaggio dal gestore di messaggi per il nuovo messaggio della finestra.</span><span class="sxs-lookup"><span data-stu-id="bca87-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bca87-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bca87-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca87-115">**Panoramica del plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="bca87-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




