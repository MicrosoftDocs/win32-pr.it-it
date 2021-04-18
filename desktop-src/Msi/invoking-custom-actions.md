---
description: Le azioni personalizzate vengono richiamate allo stesso modo delle azioni standard, tramite chiamata esplicita o durante l'esecuzione di una tabella di sequenza.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Richiamo di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318280"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="0c1c4-103">Richiamo di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="0c1c4-103">Invoking Custom Actions</span></span>

<span data-ttu-id="0c1c4-104">Le azioni personalizzate vengono richiamate allo stesso modo delle azioni standard, tramite chiamata esplicita o durante l'esecuzione di una tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="0c1c4-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="0c1c4-105">Esistono due metodi per chiamare le azioni:</span><span class="sxs-lookup"><span data-stu-id="0c1c4-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="0c1c4-106">L'azione specificata viene chiamata direttamente con la funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="0c1c4-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="0c1c4-107">Un'azione di primo livello chiama la tabella di sequenza contenente l'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0c1c4-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="0c1c4-108">Per ulteriori informazioni sulla pianificazione di un'azione personalizzata in una tabella di sequenza, vedere [sequenziazione di azioni personalizzate](sequencing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0c1c4-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="0c1c4-109">Quando il programma di installazione ottiene un nome di azione dalla funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o da una tabella Sequence, cerca innanzitutto un'azione standard con tale nome.</span><span class="sxs-lookup"><span data-stu-id="0c1c4-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="0c1c4-110">Se non riesce a trovare l'azione standard, il programma di installazione esegue una query sulla [tabella CustomAction](customaction-table.md) per verificare se l'azione specificata è un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0c1c4-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="0c1c4-111">Se l'azione specificata non è un'azione personalizzata, il programma di installazione esegue una query nella [tabella](dialog-table.md) della finestra di dialogo per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="0c1c4-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 



