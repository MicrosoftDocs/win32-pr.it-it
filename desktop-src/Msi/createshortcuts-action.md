---
description: L'azione CreateShortcuts gestisce la creazione di tasti di scelta rapida.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Azione CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058114"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="bd7d3-103">Azione CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="bd7d3-103">CreateShortcuts Action</span></span>

<span data-ttu-id="bd7d3-104">L'azione CreateShortcuts gestisce la creazione di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bd7d3-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="bd7d3-105">Sequence Restrictions</span></span>

<span data-ttu-id="bd7d3-106">L'azione CreateShortcuts deve essere successiva all'azione [InstallFiles](installfiles-action.md) e [RemoveShortcuts](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="bd7d3-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bd7d3-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="bd7d3-107">ActionData Messages</span></span>



| <span data-ttu-id="bd7d3-108">Campo</span><span class="sxs-lookup"><span data-stu-id="bd7d3-108">Field</span></span> | <span data-ttu-id="bd7d3-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="bd7d3-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="bd7d3-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bd7d3-110">\[1\]</span></span> | <span data-ttu-id="bd7d3-111">Identificatore del collegamento creato.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bd7d3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd7d3-112">Remarks</span></span>

<span data-ttu-id="bd7d3-113">L'azione CreateShortcuts crea collegamenti ai file principali dei componenti delle funzionalità selezionate per l'installazione o l'annuncio.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd7d3-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd7d3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd7d3-115">Tabella di collegamento</span><span class="sxs-lookup"><span data-stu-id="bd7d3-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="bd7d3-116">Tabella MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="bd7d3-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



