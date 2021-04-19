---
description: La tabella di estensione contiene informazioni sui server di estensione del nome di file che devono essere generati come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del registro di sistema.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabella di estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309484"
---
# <a name="extension-table"></a><span data-ttu-id="4736a-104">Tabella di estensione</span><span class="sxs-lookup"><span data-stu-id="4736a-104">Extension Table</span></span>

<span data-ttu-id="4736a-105">La tabella di estensione contiene informazioni sui server di estensione del nome di file che devono essere generati come parte dell'annuncio del prodotto.</span><span class="sxs-lookup"><span data-stu-id="4736a-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="4736a-106">Ogni riga genera un set di chiavi e valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4736a-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="4736a-107">La tabella di estensione contiene le colonne mostrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4736a-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="4736a-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="4736a-108">Column</span></span>      | <span data-ttu-id="4736a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4736a-109">Type</span></span>                         | <span data-ttu-id="4736a-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="4736a-110">Key</span></span> | <span data-ttu-id="4736a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="4736a-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="4736a-112">Estensione</span><span class="sxs-lookup"><span data-stu-id="4736a-112">Extension</span></span>   | [<span data-ttu-id="4736a-113">Text</span><span class="sxs-lookup"><span data-stu-id="4736a-113">Text</span></span>](text.md)             | <span data-ttu-id="4736a-114">S</span><span class="sxs-lookup"><span data-stu-id="4736a-114">Y</span></span>   | <span data-ttu-id="4736a-115">N</span><span class="sxs-lookup"><span data-stu-id="4736a-115">N</span></span>        |
| <span data-ttu-id="4736a-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="4736a-116">Component\_</span></span> | [<span data-ttu-id="4736a-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="4736a-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="4736a-118">S</span><span class="sxs-lookup"><span data-stu-id="4736a-118">Y</span></span>   | <span data-ttu-id="4736a-119">N</span><span class="sxs-lookup"><span data-stu-id="4736a-119">N</span></span>        |
| <span data-ttu-id="4736a-120">ProgId\_</span><span class="sxs-lookup"><span data-stu-id="4736a-120">ProgId\_</span></span>    | [<span data-ttu-id="4736a-121">Text</span><span class="sxs-lookup"><span data-stu-id="4736a-121">Text</span></span>](text.md)             | <span data-ttu-id="4736a-122">N</span><span class="sxs-lookup"><span data-stu-id="4736a-122">N</span></span>   | <span data-ttu-id="4736a-123">S</span><span class="sxs-lookup"><span data-stu-id="4736a-123">Y</span></span>        |
| <span data-ttu-id="4736a-124">MIME\_</span><span class="sxs-lookup"><span data-stu-id="4736a-124">MIME\_</span></span>      | [<span data-ttu-id="4736a-125">Text</span><span class="sxs-lookup"><span data-stu-id="4736a-125">Text</span></span>](text.md)             | <span data-ttu-id="4736a-126">N</span><span class="sxs-lookup"><span data-stu-id="4736a-126">N</span></span>   | <span data-ttu-id="4736a-127">S</span><span class="sxs-lookup"><span data-stu-id="4736a-127">Y</span></span>        |
| <span data-ttu-id="4736a-128">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="4736a-128">Feature\_</span></span>   | [<span data-ttu-id="4736a-129">Identificatore</span><span class="sxs-lookup"><span data-stu-id="4736a-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="4736a-130">N</span><span class="sxs-lookup"><span data-stu-id="4736a-130">N</span></span>   | <span data-ttu-id="4736a-131">N</span><span class="sxs-lookup"><span data-stu-id="4736a-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4736a-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="4736a-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4736a-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Estensione</span><span class="sxs-lookup"><span data-stu-id="4736a-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="4736a-134">Estensione associata alla riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="4736a-134">The extension associated with the table row.</span></span> <span data-ttu-id="4736a-135">L'estensione può avere una lunghezza di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4736a-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="4736a-136">Immettere l'estensione in questo campo senza il periodo precedente.</span><span class="sxs-lookup"><span data-stu-id="4736a-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="4736a-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="4736a-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="4736a-138">Chiave esterna per la prima colonna della tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4736a-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="4736a-139">Questa colonna fa riferimento al componente che controlla l'installazione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="4736a-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="4736a-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span><span class="sxs-lookup"><span data-stu-id="4736a-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="4736a-141">ID programma associato a questa estensione.</span><span class="sxs-lookup"><span data-stu-id="4736a-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="4736a-142">Si tratta di una chiave esterna nella tabella [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4736a-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="4736a-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span><span class="sxs-lookup"><span data-stu-id="4736a-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="4736a-144">Tipo di contenuto da scrivere per la colonna di estensione.</span><span class="sxs-lookup"><span data-stu-id="4736a-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="4736a-145">Chiave esterna per la prima colonna della tabella [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4736a-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="4736a-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="4736a-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="4736a-147">Chiave esterna nella prima colonna della tabella delle [funzionalità](feature-table.md) che specifica la funzionalità che fornisce il server di estensione.</span><span class="sxs-lookup"><span data-stu-id="4736a-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4736a-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="4736a-148">Remarks</span></span>

<span data-ttu-id="4736a-149">Viene fatto riferimento alla tabella di estensione quando viene eseguita l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) o [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4736a-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="4736a-150">Convalida</span><span class="sxs-lookup"><span data-stu-id="4736a-150">Validation</span></span>

<dl>

[<span data-ttu-id="4736a-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="4736a-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4736a-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="4736a-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4736a-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="4736a-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="4736a-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="4736a-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="4736a-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="4736a-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="4736a-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="4736a-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="4736a-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="4736a-157">ICE69</span></span>](ice69.md)  
</dl>

 

 



