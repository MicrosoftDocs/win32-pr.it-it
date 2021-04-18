---
description: L'azione CreateFolders crea cartelle vuote per i componenti impostati per l'installazione.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Azione CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319440"
---
# <a name="createfolders-action"></a><span data-ttu-id="854cb-103">Azione CreateFolders</span><span class="sxs-lookup"><span data-stu-id="854cb-103">CreateFolders Action</span></span>

<span data-ttu-id="854cb-104">L'azione CreateFolders crea cartelle vuote per i componenti impostati per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="854cb-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="854cb-105">Il programma di installazione crea cartelle per i componenti eseguiti localmente ed eseguiti dall'origine.</span><span class="sxs-lookup"><span data-stu-id="854cb-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="854cb-106">Le cartelle appena create vengono registrate con l'identificatore del componente appropriato.</span><span class="sxs-lookup"><span data-stu-id="854cb-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="854cb-107">L'azione CreateFolders esegue una query sulla [tabella CreateFolder](createfolder-table.md) e sulla [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="854cb-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="854cb-108">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="854cb-108">Sequence Restrictions</span></span>

<span data-ttu-id="854cb-109">L'azione CreateFolders deve essere eseguita prima dell'azione [InstallFiles](installfiles-action.md) o prima di qualsiasi azione che aggiunga file alle cartelle.</span><span class="sxs-lookup"><span data-stu-id="854cb-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="854cb-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="854cb-110">ActionData Messages</span></span>



| <span data-ttu-id="854cb-111">Campo</span><span class="sxs-lookup"><span data-stu-id="854cb-111">Field</span></span> | <span data-ttu-id="854cb-112">Descrizione della descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="854cb-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="854cb-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="854cb-113">\[1\]</span></span> | <span data-ttu-id="854cb-114">Identificatore di directory della cartella.</span><span class="sxs-lookup"><span data-stu-id="854cb-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="854cb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="854cb-115">Remarks</span></span>

<span data-ttu-id="854cb-116">Il programma di installazione non rimuove automaticamente le cartelle create dall'azione CreateFolders durante una disinstallazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="854cb-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="854cb-117">Il programma di installazione rimuove solo le cartelle se l' [azione RemoveFolders](removefolders-action.md) è inclusa nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="854cb-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



