---
description: L'azione WriteRegistryValori consente configura le informazioni del registro di sistema di un'applicazione.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Azione WriteRegistryValori consente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313771"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="c6ed7-103">Azione WriteRegistryValori consente</span><span class="sxs-lookup"><span data-stu-id="c6ed7-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="c6ed7-104">L'azione WriteRegistryValori consente configura le informazioni del registro di sistema di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="c6ed7-105">Le informazioni del registro di sistema sono gestite dalla [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c6ed7-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="c6ed7-106">Un valore del registro di sistema viene scritto nel registro di sistema se il componente corrispondente è stato impostato per essere installato localmente o come eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="c6ed7-107">Per altre informazioni, vedere [tabella del registro di sistema](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="c6ed7-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c6ed7-108">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="c6ed7-108">Sequence Restrictions</span></span>

<span data-ttu-id="c6ed7-109">L' [azione InstallValidate](installvalidate-action.md) deve precedere l'azione WriteRegistryValori consente.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="c6ed7-110">Se è presente un' [azione RemoveRegistryValues](removeregistryvalues-action.md), è necessario che venga eseguita prima dell'azione WriteRegistryValori consente.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="c6ed7-111">È possibile utilizzare un'azione personalizzata per aggiungere righe alla [tabella del registro di sistema](registry-table.md) durante un'installazione, una disinstallazione o una transazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="c6ed7-112">Queste righe non vengono mantenute nella tabella del registro di sistema e le informazioni sono disponibili solo durante la transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="c6ed7-113">L'azione personalizzata deve pertanto essere eseguita in ogni installazione, disinstallazione o ripristino della transazione che richiede le informazioni contenute in queste righe aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="c6ed7-114">L'azione personalizzata deve precedere le azioni [RemoveRegistryValues](removeregistryvalues-action.md) e WriteRegistryValori consente nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c6ed7-115">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="c6ed7-115">ActionData Messages</span></span>



| <span data-ttu-id="c6ed7-116">Campo</span><span class="sxs-lookup"><span data-stu-id="c6ed7-116">Field</span></span> | <span data-ttu-id="c6ed7-117">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="c6ed7-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="c6ed7-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c6ed7-118">\[1\]</span></span> | <span data-ttu-id="c6ed7-119">Percorso della chiave del registro di sistema del valore scritto nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="c6ed7-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c6ed7-120">\[2\]</span></span> | <span data-ttu-id="c6ed7-121">Nome della stringa di testo formattato del valore scritto nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="c6ed7-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="c6ed7-122">\[3\]</span></span> | <span data-ttu-id="c6ed7-123">Stringa di testo formattata del valore scritto nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ed7-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



