---
description: Dopo aver selezionato il CIEM appropriato per la convalida, lo sviluppatore deve raccogliere le azioni personalizzate in un database ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Creazione di un database di ghiaccio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881070"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="4ac3b-103">Creazione di un database di ghiaccio</span><span class="sxs-lookup"><span data-stu-id="4ac3b-103">Building an ICE Database</span></span>

<span data-ttu-id="4ac3b-104">Dopo aver selezionato il [CIEM](internal-consistency-evaluators-ices.md) appropriato per la convalida, lo sviluppatore deve raccogliere le azioni personalizzate in un database Ice.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="4ac3b-105">Un file con estensione cub è un database standard con estensione msi che contiene solo i ghiacci e le tabelle necessarie.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="4ac3b-106">Non è possibile installare un file con estensione cub e viene usato solo per archiviare e fornire l'accesso alle azioni personalizzate di ICE.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="4ac3b-107">Un file con estensione cub contiene le tabelle di database seguenti.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="4ac3b-108">Tabella</span><span class="sxs-lookup"><span data-stu-id="4ac3b-108">Table</span></span>                                  | <span data-ttu-id="4ac3b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ac3b-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ac3b-110">Binario</span><span class="sxs-lookup"><span data-stu-id="4ac3b-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="4ac3b-111">I file di script, le dll e i file exe delle azioni doganali del ghiaccio a cui viene fatto riferimento nella tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="4ac3b-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="4ac3b-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="4ac3b-113">Ogni record di questa tabella corrisponde a un'azione personalizzata ICE inclusa nel file con estensione cub.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="4ac3b-114">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="4ac3b-114">\_ICESequence</span></span>                          | <span data-ttu-id="4ac3b-115">Questa tabella elenca le azioni doganali del ghiaccio incluse nel file con estensione cub nella sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="4ac3b-116">Le azioni personalizzate ICE elencate in questa tabella vengono eseguite chiamando [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)oppure eseguite singolarmente mediante [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span><span class="sxs-lookup"><span data-stu-id="4ac3b-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="4ac3b-117">\_Convalida</span><span class="sxs-lookup"><span data-stu-id="4ac3b-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="4ac3b-118">Questa tabella contiene le voci di file con estensione cub da unire nella tabella di \_ convalida.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="4ac3b-119">\_Speciali</span><span class="sxs-lookup"><span data-stu-id="4ac3b-119">\_Special</span></span>                              | <span data-ttu-id="4ac3b-120">Tutte le tabelle di elaborazione speciali richieste da particolari azioni personalizzate del ghiaccio devono essere incluse nel file con estensione cub.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="4ac3b-121">Il nome di queste tabelle deve avere un carattere di sottolineatura principale.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="4ac3b-122">Vedere il [file Sample. cub](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="4ac3b-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ac3b-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ac3b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac3b-124">Creazione di un ghiaccio</span><span class="sxs-lookup"><span data-stu-id="4ac3b-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



