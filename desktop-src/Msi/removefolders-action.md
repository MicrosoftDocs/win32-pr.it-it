---
description: L'azione RemoveFolders rimuove tutte le cartelle collegate ai componenti impostati per la rimozione o l'esecuzione dall'origine. Queste cartelle vengono rimosse solo se sono vuote. Se una cartella viene rimossa, viene annullata la registrazione con l'identificatore del componente appropriato.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Azione RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232439"
---
# <a name="removefolders-action"></a><span data-ttu-id="d1bb0-105">Azione RemoveFolders</span><span class="sxs-lookup"><span data-stu-id="d1bb0-105">RemoveFolders Action</span></span>

<span data-ttu-id="d1bb0-106">L'azione RemoveFolders rimuove tutte le cartelle collegate ai componenti impostati per la rimozione o l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="d1bb0-107">Queste cartelle vengono rimosse solo se sono vuote.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="d1bb0-108">Se una cartella viene rimossa, viene annullata la registrazione con l'identificatore del componente appropriato.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d1bb0-109">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="d1bb0-109">Sequence Restrictions</span></span>

<span data-ttu-id="d1bb0-110">L'azione RemoveFolders deve provenire dopo l'azione [RemoveFiles](removefiles-action.md) o qualsiasi azione che potrebbe rimuovere file dalle cartelle.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d1bb0-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="d1bb0-111">ActionData Messages</span></span>



| <span data-ttu-id="d1bb0-112">Campo</span><span class="sxs-lookup"><span data-stu-id="d1bb0-112">Field</span></span> | <span data-ttu-id="d1bb0-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="d1bb0-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="d1bb0-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d1bb0-114">\[1\]</span></span> | <span data-ttu-id="d1bb0-115">Identificatore della cartella rimossa.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d1bb0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1bb0-116">Remarks</span></span>

<span data-ttu-id="d1bb0-117">Il programma di installazione non rimuove automaticamente le cartelle create dall' [azione CreateFolders](createfolders-action.md) durante una disinstallazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="d1bb0-118">È necessario indicare al programma di installazione di rimuovere queste cartelle creando l'azione RemoveFolders nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="d1bb0-119">Per specificare il nome e il percorso della cartella, utilizzare la \_ colonna directory della [tabella CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb0-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="d1bb0-120">Si presuppone che ogni nome di cartella nella tabella CreateFolder sia una proprietà che definisce il percorso della cartella.</span><span class="sxs-lookup"><span data-stu-id="d1bb0-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="d1bb0-121">Per specificare il componente proprietario della cartella, utilizzare la colonna ComponentId della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb0-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



