---
description: La tabella ProgId contiene informazioni per gli ID programma e gli ID del programma indipendenti dalla versione che devono essere generati come parte dell'annuncio del prodotto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabella ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968510"
---
# <a name="progid-table"></a><span data-ttu-id="f1896-103">Tabella ProgId</span><span class="sxs-lookup"><span data-stu-id="f1896-103">ProgId Table</span></span>

<span data-ttu-id="f1896-104">La tabella ProgId contiene informazioni per gli ID programma e gli ID del programma indipendenti dalla versione che devono essere generati come parte dell'annuncio del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f1896-104">The ProgId table contains information for program IDs and version independent program IDs that must be generated as a part of the product advertisement.</span></span>

<span data-ttu-id="f1896-105">La tabella ProgId contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1896-105">The ProgId table has the following columns.</span></span>



| <span data-ttu-id="f1896-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="f1896-106">Column</span></span>         | <span data-ttu-id="f1896-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1896-107">Type</span></span>                         | <span data-ttu-id="f1896-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="f1896-108">Key</span></span> | <span data-ttu-id="f1896-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f1896-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="f1896-110">ProgId</span><span class="sxs-lookup"><span data-stu-id="f1896-110">ProgId</span></span>         | [<span data-ttu-id="f1896-111">Text</span><span class="sxs-lookup"><span data-stu-id="f1896-111">Text</span></span>](text.md)             | <span data-ttu-id="f1896-112">S</span><span class="sxs-lookup"><span data-stu-id="f1896-112">Y</span></span>   | <span data-ttu-id="f1896-113">N</span><span class="sxs-lookup"><span data-stu-id="f1896-113">N</span></span>        |
| <span data-ttu-id="f1896-114">ProgId \_ padre</span><span class="sxs-lookup"><span data-stu-id="f1896-114">ProgId\_Parent</span></span> | [<span data-ttu-id="f1896-115">Text</span><span class="sxs-lookup"><span data-stu-id="f1896-115">Text</span></span>](text.md)             | <span data-ttu-id="f1896-116">N</span><span class="sxs-lookup"><span data-stu-id="f1896-116">N</span></span>   | <span data-ttu-id="f1896-117">S</span><span class="sxs-lookup"><span data-stu-id="f1896-117">Y</span></span>        |
| <span data-ttu-id="f1896-118">Classe\_</span><span class="sxs-lookup"><span data-stu-id="f1896-118">Class\_</span></span>        | [<span data-ttu-id="f1896-119">GUID</span><span class="sxs-lookup"><span data-stu-id="f1896-119">GUID</span></span>](guid.md)             | <span data-ttu-id="f1896-120">N</span><span class="sxs-lookup"><span data-stu-id="f1896-120">N</span></span>   | <span data-ttu-id="f1896-121">S</span><span class="sxs-lookup"><span data-stu-id="f1896-121">Y</span></span>        |
| <span data-ttu-id="f1896-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1896-122">Description</span></span>    | [<span data-ttu-id="f1896-123">Text</span><span class="sxs-lookup"><span data-stu-id="f1896-123">Text</span></span>](text.md)             | <span data-ttu-id="f1896-124">N</span><span class="sxs-lookup"><span data-stu-id="f1896-124">N</span></span>   | <span data-ttu-id="f1896-125">S</span><span class="sxs-lookup"><span data-stu-id="f1896-125">Y</span></span>        |
| <span data-ttu-id="f1896-126">Icona\_</span><span class="sxs-lookup"><span data-stu-id="f1896-126">Icon\_</span></span>         | [<span data-ttu-id="f1896-127">Identificatore</span><span class="sxs-lookup"><span data-stu-id="f1896-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="f1896-128">N</span><span class="sxs-lookup"><span data-stu-id="f1896-128">N</span></span>   | <span data-ttu-id="f1896-129">S</span><span class="sxs-lookup"><span data-stu-id="f1896-129">Y</span></span>        |
| <span data-ttu-id="f1896-130">IconIndex</span><span class="sxs-lookup"><span data-stu-id="f1896-130">IconIndex</span></span>      | [<span data-ttu-id="f1896-131">Integer</span><span class="sxs-lookup"><span data-stu-id="f1896-131">Integer</span></span>](integer.md)       | <span data-ttu-id="f1896-132">N</span><span class="sxs-lookup"><span data-stu-id="f1896-132">N</span></span>   | <span data-ttu-id="f1896-133">S</span><span class="sxs-lookup"><span data-stu-id="f1896-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f1896-134">Colonne</span><span class="sxs-lookup"><span data-stu-id="f1896-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f1896-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span><span class="sxs-lookup"><span data-stu-id="f1896-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span></span>
</dt> <dd>

<span data-ttu-id="f1896-136">ID del programma o ID del programma indipendente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="f1896-136">The program ID or version independent program ID.</span></span> <span data-ttu-id="f1896-137">I ProgId elencati nella tabella ProgId vengono registrati se il CLSID elencato nella \_ colonna classe di questa tabella è pianificato per l'annuncio o l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f1896-137">ProgIds listed in the ProgId table are registered if the CLSID listed in the Class\_column of this table is scheduled to be advertised or installed.</span></span> <span data-ttu-id="f1896-138">Quando il ProgId è selezionato per la registrazione, tutti i ProgId che fanno riferimento a questa riga tramite la \_ colonna padre ProgID sono selezionati anche per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="f1896-138">When the ProgId is selected for registration, all ProgIds that refer to this row through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="f1896-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ padre</span><span class="sxs-lookup"><span data-stu-id="f1896-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="f1896-140">Definito solo per gli ID del programma indipendenti dalla versione.</span><span class="sxs-lookup"><span data-stu-id="f1896-140">Defined only for version independent program IDs.</span></span> <span data-ttu-id="f1896-141">Questo campo è una chiave esterna nella colonna ProgId.</span><span class="sxs-lookup"><span data-stu-id="f1896-141">This field is a foreign key into the ProgId column.</span></span> <span data-ttu-id="f1896-142">Per definire un ID del programma indipendente dalla versione, immettere il ProgId corrispondente nella \_ colonna padre ProgID.</span><span class="sxs-lookup"><span data-stu-id="f1896-142">To define a version independent program ID, enter the corresponding ProgId into the ProgId\_Parent column.</span></span> <span data-ttu-id="f1896-143">Quando il ProgId è selezionato per l'installazione, vengono selezionati anche i ProgId corrispondenti indipendenti dalla versione associati tramite la \_ colonna padre ProgID per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="f1896-143">When the ProgId is selected for installation, the corresponding version-independent ProgIds associated through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="f1896-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Classe\_</span><span class="sxs-lookup"><span data-stu-id="f1896-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Class\_</span></span>
</dt> <dd>

<span data-ttu-id="f1896-145">Chiave esterna facoltativa nella [tabella della classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="f1896-145">An optional foreign key into the [Class table](class-table.md).</span></span> <span data-ttu-id="f1896-146">Questa colonna deve essere null per un ProgId indipendente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="f1896-146">This column must be Null for a version independent ProgId.</span></span> <span data-ttu-id="f1896-147">Se il valore della classe \_ per un ProgID è null, il ProgID viene registrato quando viene visualizzato nella colonna ProgID di una riga nella [tabella di estensione](extension-table.md) e all'estensione è associato almeno un verbo nella [tabella dei verbi](verb-table.md).</span><span class="sxs-lookup"><span data-stu-id="f1896-147">If the Class\_value for a ProgId is null, the ProgId is registered when it appears in the ProgId column of a row in the [Extension table](extension-table.md) and the extension has at least one Verb associated with it in the [Verb table](verb-table.md).</span></span> <span data-ttu-id="f1896-148">I ProgId selezionati per la registrazione in questo modo non installano altri ProgId che fanno riferimento al ProgId corrente tramite il \_ valore predefinito ProgID.</span><span class="sxs-lookup"><span data-stu-id="f1896-148">ProgIds selected for registration in this manner do not install other ProgIds that reference the current ProgId through the ProgId\_Default value.</span></span>

</dd> <dt>

<span data-ttu-id="f1896-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1896-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="f1896-150">Descrizione localizzata facoltativa dell'ID del programma associato.</span><span class="sxs-lookup"><span data-stu-id="f1896-150">An optional localized description of the associated program ID.</span></span>

</dd> <dt>

<span data-ttu-id="f1896-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_</span><span class="sxs-lookup"><span data-stu-id="f1896-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="f1896-152">Chiave esterna facoltativa nella [tabella delle icone](icon-table.md) che specifica il file icona associato a questo ProgID.</span><span class="sxs-lookup"><span data-stu-id="f1896-152">An optional foreign key into the [Icon table](icon-table.md) that specifies the icon file associated with this ProgId.</span></span> <span data-ttu-id="f1896-153">Questa operazione viene scritta sotto la chiave DefaultIcon associata a questo ProgId.</span><span class="sxs-lookup"><span data-stu-id="f1896-153">This is written under the DefaultIcon key associated with this ProgId.</span></span> <span data-ttu-id="f1896-154">Questa colonna deve essere null per un ProgId indipendente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="f1896-154">This column must be Null for a version independent ProgId.</span></span>

</dd> <dt>

<span data-ttu-id="f1896-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="f1896-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="f1896-156">Indice dell'icona nel file icona.</span><span class="sxs-lookup"><span data-stu-id="f1896-156">The Icon index into the icon file.</span></span> <span data-ttu-id="f1896-157">Questa colonna deve essere null per un ProgId indipendente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="f1896-157">This column must be Null for a version independent ProgId.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1896-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1896-158">Remarks</span></span>

<span data-ttu-id="f1896-159">Le azioni [RegisterProgIdInfo](registerprogidinfo-action.md) e [UnregisterProgIdInfo](unregisterprogidinfo-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="f1896-159">The [RegisterProgIdInfo](registerprogidinfo-action.md) and [UnregisterProgIdInfo](unregisterprogidinfo-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f1896-160">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f1896-160">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f1896-161">Convalida</span><span class="sxs-lookup"><span data-stu-id="f1896-161">Validation</span></span>

<dl>

[<span data-ttu-id="f1896-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="f1896-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f1896-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="f1896-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f1896-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="f1896-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f1896-165">ICE36</span><span class="sxs-lookup"><span data-stu-id="f1896-165">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="f1896-166">ICE89</span><span class="sxs-lookup"><span data-stu-id="f1896-166">ICE89</span></span>](ice89.md)  
</dl>

 

 



