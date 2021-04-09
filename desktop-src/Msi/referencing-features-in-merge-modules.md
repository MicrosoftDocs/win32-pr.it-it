---
description: I moduli merge operano solo con componenti e non con funzionalità. Tuttavia, alcune tabelle nei moduli merge, ad esempio la tabella PublishComponent, contengono campi che fanno riferimento alle funzionalità.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Riferimenti alle funzionalità nei moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967410"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="79e05-104">Riferimenti alle funzionalità nei moduli merge</span><span class="sxs-lookup"><span data-stu-id="79e05-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="79e05-105">I moduli merge operano solo con componenti e non con funzionalità.</span><span class="sxs-lookup"><span data-stu-id="79e05-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="79e05-106">Tuttavia, alcune tabelle nei moduli merge, ad esempio la [tabella PublishComponent](publishcomponent-table.md), contengono campi che fanno riferimento alle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="79e05-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="79e05-107">Un GUID null: {00000000-0000-0000-0000-000000000000} deve essere creato in qualsiasi campo di un database del modulo merge che fa riferimento a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="79e05-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="79e05-108">Quando il modulo merge viene unito in un pacchetto di installazione, lo strumento merge sostituisce il GUID null con la funzionalità specificata nel pacchetto di installazione, ad eccezione delle tabelle che richiedono una gestione speciale, ad esempio la [tabella ModuleSignature](modulesignature-table.md) e le tabelle ModuleSequence.</span><span class="sxs-lookup"><span data-stu-id="79e05-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="79e05-109">Si noti che se un GUID null viene utilizzato come chiave primaria, non è garantito che il valore sostituito dallo strumento di merge sia univoco.</span><span class="sxs-lookup"><span data-stu-id="79e05-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="79e05-110">Gli autori dei moduli merge sono responsabili di garantire che nessuna chiave primaria esistente nell'interfaccia dell'utente venga duplicata quando lo strumento di Unione sostituisce i GUID null con le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="79e05-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



