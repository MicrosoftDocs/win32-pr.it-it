---
description: Una funzione del programma di installazione può visualizzare una finestra di dialogo di messaggio di errore che restituisce uno degli errori seguenti. Una casella di errore viene visualizzata solo se il livello dell'interfaccia utente è a livello completo, ridotto o di base. Per ulteriori informazioni, vedere livelli di interfaccia utente.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Messaggi di errore visualizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309498"
---
# <a name="displayed-error-messages"></a><span data-ttu-id="c9318-105">Messaggi di errore visualizzati</span><span class="sxs-lookup"><span data-stu-id="c9318-105">Displayed Error Messages</span></span>

<span data-ttu-id="c9318-106">Una [funzione del programma di installazione](installer-function-reference.md) può visualizzare una finestra di dialogo di messaggio di errore che restituisce uno degli errori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9318-106">An [installer function](installer-function-reference.md) may display an error message dialog box returning any of the following errors.</span></span> <span data-ttu-id="c9318-107">Una casella di errore viene visualizzata solo se il livello dell'interfaccia utente è a livello completo, ridotto o di base.</span><span class="sxs-lookup"><span data-stu-id="c9318-107">An error box is displayed only if the user interface level is at the full, reduced, or basic level.</span></span> <span data-ttu-id="c9318-108">Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c9318-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="c9318-109">Le funzioni del programma di installazione visualizzano solo i messaggi di errore riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c9318-109">The installer functions only display error messages that are in the following table.</span></span> <span data-ttu-id="c9318-110">Per gli errori non presenti nell'elenco, il chiamante della funzione è responsabile della gestione della visualizzazione dei messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="c9318-110">For errors not in this list, the caller of the function is responsible for handling the display of error messages.</span></span>



| <span data-ttu-id="c9318-111">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="c9318-111">Error code</span></span>               | <span data-ttu-id="c9318-112">Errore</span><span class="sxs-lookup"><span data-stu-id="c9318-112">Error</span></span>                        |
|--------------------------|------------------------------|
| <span data-ttu-id="c9318-113">ERRORE \_ installazione \_ sospensione</span><span class="sxs-lookup"><span data-stu-id="c9318-113">ERROR\_INSTALL\_SUSPEND</span></span>  | <span data-ttu-id="c9318-114">L'installazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="c9318-114">The install was suspended.</span></span>   |
| <span data-ttu-id="c9318-115">ERRORE di \_ installazione di \_ USEREXIT</span><span class="sxs-lookup"><span data-stu-id="c9318-115">ERROR\_INSTALL\_USEREXIT</span></span> | <span data-ttu-id="c9318-116">L'utente ha terminato l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c9318-116">The user exited the install.</span></span> |
| <span data-ttu-id="c9318-117">ERRORE di \_ installazione \_</span><span class="sxs-lookup"><span data-stu-id="c9318-117">ERROR\_INSTALL\_FAILURE</span></span>  | <span data-ttu-id="c9318-118">Installazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="c9318-118">Install failed.</span></span>              |



 

 

 



