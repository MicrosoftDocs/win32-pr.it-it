---
description: ICE44 verifica che NewDialog, SpawnDialog e SpawnWaitDialog ControlEvents facciano riferimento a finestre di dialogo valide nella tabella della finestra di dialogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314212"
---
# <a name="ice44"></a><span data-ttu-id="a26a0-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="a26a0-103">ICE44</span></span>

<span data-ttu-id="a26a0-104">ICE44 verifica che [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)e [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents facciano riferimento a finestre di dialogo valide nella [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="a26a0-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="a26a0-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="a26a0-105">Result</span></span>

<span data-ttu-id="a26a0-106">ICE44 Invia un messaggio di errore se è presente un evento di controllo della finestra di dialogo che non fa riferimento a una finestra di dialogo elencata nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a26a0-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="a26a0-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="a26a0-107">Example</span></span>

<span data-ttu-id="a26a0-108">ICE44 segnala gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="a26a0-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="a26a0-109">Errore ICE44</span><span class="sxs-lookup"><span data-stu-id="a26a0-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="a26a0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a26a0-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a26a0-111">Evento di controllo per il controllo ' Dialog1' .' Control1' è di tipo SpawnDialog, ma il relativo argomento Dialog2 non è una voce valida nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a26a0-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="a26a0-112">Sono presenti azioni SpawnDialog, SpawnWaitDialog o NewDialog con un argomento che non fa riferimento a una finestra di dialogo nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a26a0-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="a26a0-113">Per correggere l'errore, aggiungere un argomento che rappresenta una chiave nella tabella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a26a0-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="a26a0-114">[Tabella finestra di dialogo](dialog-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="a26a0-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="a26a0-115">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="a26a0-115">Dialog</span></span>  | <span data-ttu-id="a26a0-116">Titolo</span><span class="sxs-lookup"><span data-stu-id="a26a0-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="a26a0-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="a26a0-117">Dialog1</span></span> |       |



 

<span data-ttu-id="a26a0-118">[Tabella ControlEvent](controlevent-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="a26a0-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="a26a0-119">Finestra di dialogo\_</span><span class="sxs-lookup"><span data-stu-id="a26a0-119">Dialog\_</span></span> | <span data-ttu-id="a26a0-120">controllo\_</span><span class="sxs-lookup"><span data-stu-id="a26a0-120">Control\_</span></span> | <span data-ttu-id="a26a0-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a26a0-121">Type</span></span>        | <span data-ttu-id="a26a0-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="a26a0-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="a26a0-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="a26a0-123">Dialog1</span></span>  | <span data-ttu-id="a26a0-124">Control1</span><span class="sxs-lookup"><span data-stu-id="a26a0-124">Control1</span></span>  | <span data-ttu-id="a26a0-125">SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="a26a0-125">SpawnDialog</span></span> | <span data-ttu-id="a26a0-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="a26a0-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="a26a0-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a26a0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a26a0-128">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="a26a0-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




