---
description: Quando un modulo supporta più lingue, è possibile eseguirne il merge nello stesso database di Windows Installer più volte, ma assicurarsi che ogni merge usi una lingua diversa.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Unione di un modulo a più lingue nello stesso pacchetto più volte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315900"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="e42bc-103">Unione di un modulo a più lingue nello stesso pacchetto più volte</span><span class="sxs-lookup"><span data-stu-id="e42bc-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="e42bc-104">Quando un modulo supporta più lingue, è possibile eseguirne il merge nello stesso database di Windows Installer più volte, ma assicurarsi che ogni merge usi una lingua diversa.</span><span class="sxs-lookup"><span data-stu-id="e42bc-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="e42bc-105">Prima di ogni Unione, richiedere una lingua diversa dal modulo.</span><span class="sxs-lookup"><span data-stu-id="e42bc-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="e42bc-106">Il database con estensione MSI risultante dispone quindi di un record nella [tabella ModuleSignature](modulesignature-table.md) per ogni unione del modulo.</span><span class="sxs-lookup"><span data-stu-id="e42bc-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="e42bc-107">I componenti condivisi tra i linguaggi sono disponibili solo una volta nella [tabella dei componenti](component-table.md), ma sono associati a ogni lingua nella [tabella ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="e42bc-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="e42bc-108">Quando si uniscono più lingue di un modulo nello stesso pacchetto, ogni Unione deve soddisfare le stesse restrizioni sulle tabelle codici come moduli a linguaggio singolo.</span><span class="sxs-lookup"><span data-stu-id="e42bc-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="e42bc-109">I moduli non possono contenere stringhe in tabelle codici diverse.</span><span class="sxs-lookup"><span data-stu-id="e42bc-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="e42bc-110">Quando si unisce un modulo più volte in un unico file con estensione msi, potrebbe essere necessario modificare l'ordine dei file nella [tabella file](file-table.md) in modo da usare il file con estensione CAB esistente dal modulo direttamente nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="e42bc-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="e42bc-111">L'ordine dei file nella tabella file deve corrispondere all'ordine dei file nel file con estensione cab.</span><span class="sxs-lookup"><span data-stu-id="e42bc-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="e42bc-112">Quando si unisce un modulo più volte in un database di installazione, la sequenza può essere modificata, perché i file condivisi tra le lingue potrebbero già esistere nel modulo da un'unione precedente e hanno un numero di sequenza relativo diverso.</span><span class="sxs-lookup"><span data-stu-id="e42bc-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 



