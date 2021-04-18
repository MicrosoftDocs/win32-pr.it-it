---
description: È possibile utilizzare le funzioni del programma di installazione per eseguire azioni specifiche o sequenze di azioni.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Azioni in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309452"
---
# <a name="running-actions"></a><span data-ttu-id="81289-103">Azioni in esecuzione</span><span class="sxs-lookup"><span data-stu-id="81289-103">Running Actions</span></span>

<span data-ttu-id="81289-104">È possibile utilizzare le funzioni del programma di installazione per eseguire azioni specifiche o sequenze di azioni.</span><span class="sxs-lookup"><span data-stu-id="81289-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="81289-105">Queste azioni possono essere azioni [standard](standard-actions.md) o [personalizzate](custom-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="81289-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="81289-106">Nella procedura seguente viene descritto come eseguire le azioni:</span><span class="sxs-lookup"><span data-stu-id="81289-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="81289-107">**Per eseguire una sequenza di azione**</span><span class="sxs-lookup"><span data-stu-id="81289-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="81289-108">Eseguire una sequenza di azioni definite in una tabella chiamando la funzione [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .</span><span class="sxs-lookup"><span data-stu-id="81289-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="81289-109">Il programma di installazione esegue una query sulla tabella indicata ed esegue ogni azione se la relativa espressione condizionale restituisce TRUE.</span><span class="sxs-lookup"><span data-stu-id="81289-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="81289-110">Controllare le espressioni condizionali chiamando la funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="81289-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="81289-111">Eseguire l'azione chiamando la funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="81289-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="81289-112">L'azione può essere un'azione standard, un'azione personalizzata o una finestra di dialogo dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="81289-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="81289-113">Se si è verificato un errore durante l'esecuzione di questa azione, chiamare la funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="81289-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="81289-114">L'errore verrà elaborato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="81289-114">The installer will process the error.</span></span>

 

 



