---
description: L'azione IsolateComponents installa una copia di un componente (in genere una DLL condivisa) in una posizione privata per l'uso da parte di un'applicazione specifica, in genere un file con estensione exe.
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Azione IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348981"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="f936f-103">Azione IsolateComponents</span><span class="sxs-lookup"><span data-stu-id="f936f-103">IsolateComponents Action</span></span>

<span data-ttu-id="f936f-104">L'azione IsolateComponents installa una copia di un componente (in genere una DLL condivisa) in una posizione privata per l'uso da parte di un'applicazione specifica, in genere un file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="f936f-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="f936f-105">Questo consente di isolare l'applicazione da altre copie del componente che possono essere installate in un percorso condiviso nel computer.</span><span class="sxs-lookup"><span data-stu-id="f936f-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="f936f-106">Per ulteriori informazioni, vedere [componenti isolati](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="f936f-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="f936f-107">L'azione fa riferimento a ogni record della [tabella IsolatedComponent](isolatedcomponent-table.md) e associa i file del componente elencato nel \_ campo Shared Component con il componente elencato nel \_ campo applicazione componente.</span><span class="sxs-lookup"><span data-stu-id="f936f-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="f936f-108">Il programma di installazione installa i file di componente \_ condivisi nella stessa directory dell' \_ applicazione Component.</span><span class="sxs-lookup"><span data-stu-id="f936f-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="f936f-109">Il programma di installazione genera un file in questa directory, con una lunghezza pari a zero byte, con il nome di nome file breve del file di chiave per l' \_ applicazione componente (in genere si tratta dello stesso nome del file con estensione exe) aggiunto con. local.</span><span class="sxs-lookup"><span data-stu-id="f936f-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="f936f-110">L'azione IsolatedComponent non influisce sull'installazione dell' \_ applicazione Component.</span><span class="sxs-lookup"><span data-stu-id="f936f-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="f936f-111">La disinstallazione dell' \_ applicazione componente consente inoltre di rimuovere i \_ file condivisi del componente e il file. local dalla directory.</span><span class="sxs-lookup"><span data-stu-id="f936f-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f936f-112">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="f936f-112">Sequence Restrictions</span></span>

<span data-ttu-id="f936f-113">L'azione IsolateComponents può essere utilizzata solo nella [tabella InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f936f-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="f936f-114">Questa azione deve essere successiva all'azione [CostInitialize](costinitialize-action.md) e prima dell' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f936f-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f936f-115">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="f936f-115">ActionData Messages</span></span>

<span data-ttu-id="f936f-116">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="f936f-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f936f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f936f-117">Remarks</span></span>

<span data-ttu-id="f936f-118">Se la colonna Condition per l'azione IsolateComponents restituisce true o viene lasciato vuoto, il programma di installazione isola tutti i componenti elencati nella [tabella IsolatedComponent](isolatedcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f936f-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="f936f-119">Se la colonna Condition restituisce false, il programma di installazione ignora la tabella IsolatedComponent e condivide i componenti normalmente.</span><span class="sxs-lookup"><span data-stu-id="f936f-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="f936f-120">Per condizionare questa azione, è possibile usare la proprietà [**RedirectedDllSupport**](redirecteddllsupport.md) .</span><span class="sxs-lookup"><span data-stu-id="f936f-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="f936f-121">Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f936f-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



