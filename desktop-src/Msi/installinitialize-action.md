---
description: L'azione InstallInitialize e l'azione InstallFinalize contrassegnano l'inizio e la fine di una sequenza di azioni che modificano il sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Azione InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752202"
---
# <a name="installinitialize-action"></a><span data-ttu-id="2660a-103">Azione InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="2660a-103">InstallInitialize Action</span></span>

<span data-ttu-id="2660a-104">L'azione InstallInitialize e l'azione [InstallFinalize](installfinalize-action.md) contrassegnano l'inizio e la fine di una sequenza di azioni che modificano il sistema.</span><span class="sxs-lookup"><span data-stu-id="2660a-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2660a-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="2660a-105">Sequence Restrictions</span></span>

<span data-ttu-id="2660a-106">L'azione InstallInitialize deve essere sequenziata prima di qualsiasi azione che modifichi il sistema, ad esempio l'azione [InstallFiles](installfiles-action.md) , l'azione [WriteRegistryValori consente](writeregistryvalues-action.md) , l'azione [SelfRegModules](selfregmodules-action.md) e l'azione [ProcessComponents](processcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2660a-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="2660a-107">L'azione InstallInitialize deve quindi essere sequenziata prima dell'azione [InstallFinalize](installfinalize-action.md) e [InstallExecute](installexecute-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2660a-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="2660a-108">Le [azioni personalizzate](custom-actions.md) che modificano il pacchetto di Windows Installer, ad esempio l'aggiunta di righe a una tabella che gestisce le risorse installabili, ad esempio la tabella [del registro di sistema](registry-table.md) o la tabella [DuplicateFile](duplicatefile-table.md) , devono essere sequenziate prima dell'azione InstallInitialize.</span><span class="sxs-lookup"><span data-stu-id="2660a-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2660a-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="2660a-109">ActionData Messages</span></span>

<span data-ttu-id="2660a-110">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="2660a-110">There are no ActionData messages.</span></span>

 

 



