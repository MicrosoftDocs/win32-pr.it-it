---
description: ICE26 convalida le tabelle di sequenza in un database Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882937"
---
# <a name="ice26"></a><span data-ttu-id="30206-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="30206-103">ICE26</span></span>

<span data-ttu-id="30206-104">ICE26 verifica che ognuna delle [*tabelle di sequenza*](s-gly.md) seguenti contenga le azioni necessarie per la tabella e non contenga alcuna azione non consentita nella tabella:</span><span class="sxs-lookup"><span data-stu-id="30206-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="30206-105">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="30206-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="30206-106">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="30206-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="30206-107">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="30206-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="30206-108">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="30206-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="30206-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="30206-109">Result</span></span>

<span data-ttu-id="30206-110">ICE26 Invia un messaggio di errore se il pacchetto di installazione dispone di una tabella di sequenza in cui manca un'azione obbligatoria o che contiene un'azione non consentita per la tabella.</span><span class="sxs-lookup"><span data-stu-id="30206-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="30206-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="30206-111">Example</span></span>



| <span data-ttu-id="30206-112">Errore ICE26</span><span class="sxs-lookup"><span data-stu-id="30206-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="30206-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30206-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30206-114">Azione:' action1' è obbligatorio nella tabella di sequenza InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="30206-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="30206-115">Manca un'azione obbligatoria nella tabella di sequenza indicata.</span><span class="sxs-lookup"><span data-stu-id="30206-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="30206-116">Vedere l'template.msi o le tabelle di sequenza suggerite in [uso di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="30206-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="30206-117">Azione:' Action2' non è consentito nella tabella di sequenza InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="30206-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="30206-118">Questa azione non può essere inclusa nella tabella di sequenza indicata.</span><span class="sxs-lookup"><span data-stu-id="30206-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="30206-119">Rimuovere questa azione dalla tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="30206-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="30206-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30206-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30206-121">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="30206-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



