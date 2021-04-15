---
description: La tabella ModuleSignature è una tabella obbligatoria.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Tabella ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529244"
---
# <a name="modulesignature-table"></a><span data-ttu-id="cb2ae-103">Tabella ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="cb2ae-103">ModuleSignature Table</span></span>

<span data-ttu-id="cb2ae-104">La tabella ModuleSignature è una tabella obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="cb2ae-105">Contiene tutte le informazioni necessarie per identificare un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="cb2ae-106">Lo strumento merge aggiunge questa tabella al file con estensione msi, se non ne esiste già una.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="cb2ae-107">La tabella ModuleSignature in un modulo merge include solo una riga contenente ModuleID, Language e Version.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="cb2ae-108">Tuttavia, la tabella ModuleSignature in un file con estensione msi include una riga contenente queste informazioni per ogni file con estensione MSM di cui è stato eseguito il merge.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="cb2ae-109">Strumenti di merge e verifica controllare la tabella ModuleSignature nei file con estensione msi per determinare se sono presenti tutti i moduli merge dipendenti richiesti dal modulo merge corrente (vedere la [tabella ModuleDependency](moduledependency-table.md)) e se il pacchetto di installazione è stato precedentemente Unito a eventuali moduli merge in conflitto (vedere la [tabella ModuleExclusion](moduleexclusion-table.md)).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="cb2ae-110">La tabella ModuleSignature include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="cb2ae-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="cb2ae-111">Column</span></span>   | <span data-ttu-id="cb2ae-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb2ae-112">Type</span></span>                         | <span data-ttu-id="cb2ae-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="cb2ae-113">Key</span></span> | <span data-ttu-id="cb2ae-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="cb2ae-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="cb2ae-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="cb2ae-115">ModuleID</span></span> | [<span data-ttu-id="cb2ae-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="cb2ae-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="cb2ae-117">S</span><span class="sxs-lookup"><span data-stu-id="cb2ae-117">Y</span></span>   | <span data-ttu-id="cb2ae-118">N</span><span class="sxs-lookup"><span data-stu-id="cb2ae-118">N</span></span>        |
| <span data-ttu-id="cb2ae-119">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="cb2ae-119">Language</span></span> | [<span data-ttu-id="cb2ae-120">Integer</span><span class="sxs-lookup"><span data-stu-id="cb2ae-120">Integer</span></span>](integer.md)       | <span data-ttu-id="cb2ae-121">S</span><span class="sxs-lookup"><span data-stu-id="cb2ae-121">Y</span></span>   | <span data-ttu-id="cb2ae-122">N</span><span class="sxs-lookup"><span data-stu-id="cb2ae-122">N</span></span>        |
| <span data-ttu-id="cb2ae-123">Versione</span><span class="sxs-lookup"><span data-stu-id="cb2ae-123">Version</span></span>  | [<span data-ttu-id="cb2ae-124">Versione</span><span class="sxs-lookup"><span data-stu-id="cb2ae-124">Version</span></span>](version.md)       |     | <span data-ttu-id="cb2ae-125">N</span><span class="sxs-lookup"><span data-stu-id="cb2ae-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cb2ae-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="cb2ae-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cb2ae-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="cb2ae-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="cb2ae-128">Identificatore che identifica in modo univoco il modulo unione.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="cb2ae-129">Due moduli merge non possono avere lo stesso ModuleID, a meno che il modulo merge non sia completamente compatibile con il relativo predecessore.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="cb2ae-130">È possibile creare un GUID per questo campo usando un'utilità, ad esempio GUIDGEN.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="cb2ae-131">La colonna ModuleID è una chiave primaria per la tabella e pertanto deve seguire la convenzione di denominazione per la [denominazione delle chiavi primarie nei database del modulo merge](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="cb2ae-132">Se, ad esempio, il nome leggibile del modulo merge è MyLibrary e il GUID è {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la voce nella colonna ModuleID diventa MyLibrary. 880DE2F0 \_ CDD8 11D1 A849 \_ 006097ABDE17 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cb2ae-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="cb2ae-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio</span><span class="sxs-lookup"><span data-stu-id="cb2ae-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="cb2ae-134">L'identificatore di lingua specifica la lingua predefinita per il modulo unione.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="cb2ae-135">L'identificatore di lingua è in formato decimale, ad esempio l'inglese (Stati Uniti) è 1033.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="cb2ae-136">Il linguaggio utilizzato dal modulo merge può essere modificato applicando una trasformazione al modulo merge prima dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="cb2ae-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione</span><span class="sxs-lookup"><span data-stu-id="cb2ae-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="cb2ae-138">Il campo versione contiene una stringa che descrive le versioni principale e secondaria del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="cb2ae-139">Convalida</span><span class="sxs-lookup"><span data-stu-id="cb2ae-139">Validation</span></span>

<dl>

[<span data-ttu-id="cb2ae-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="cb2ae-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cb2ae-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="cb2ae-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cb2ae-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="cb2ae-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="cb2ae-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb2ae-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb2ae-144">Moduli unione a più lingue</span><span class="sxs-lookup"><span data-stu-id="cb2ae-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



