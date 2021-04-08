---
description: La tabella ReserveCost è una tabella facoltativa che consente all'autore di riservare una quantità di spazio su disco in qualsiasi directory che dipende dallo stato di installazione di un componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Tabella ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967734"
---
# <a name="reservecost-table"></a><span data-ttu-id="7745b-103">Tabella ReserveCost</span><span class="sxs-lookup"><span data-stu-id="7745b-103">ReserveCost Table</span></span>

<span data-ttu-id="7745b-104">La tabella ReserveCost è una tabella facoltativa che consente all'autore di riservare una quantità di spazio su disco in qualsiasi directory che dipende dallo stato di installazione di un componente.</span><span class="sxs-lookup"><span data-stu-id="7745b-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="7745b-105">La tabella ReserveCost include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="7745b-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="7745b-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="7745b-106">Column</span></span>        | <span data-ttu-id="7745b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7745b-107">Type</span></span>                               | <span data-ttu-id="7745b-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="7745b-108">Key</span></span> | <span data-ttu-id="7745b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7745b-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="7745b-110">ReserveKey</span><span class="sxs-lookup"><span data-stu-id="7745b-110">ReserveKey</span></span>    | [<span data-ttu-id="7745b-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7745b-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="7745b-112">S</span><span class="sxs-lookup"><span data-stu-id="7745b-112">Y</span></span>   | <span data-ttu-id="7745b-113">N</span><span class="sxs-lookup"><span data-stu-id="7745b-113">N</span></span>        |
| <span data-ttu-id="7745b-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7745b-114">Component\_</span></span>   | [<span data-ttu-id="7745b-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7745b-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="7745b-116">N</span><span class="sxs-lookup"><span data-stu-id="7745b-116">N</span></span>   | <span data-ttu-id="7745b-117">N</span><span class="sxs-lookup"><span data-stu-id="7745b-117">N</span></span>        |
| <span data-ttu-id="7745b-118">ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="7745b-118">ReserveFolder</span></span> | [<span data-ttu-id="7745b-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="7745b-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="7745b-120">N</span><span class="sxs-lookup"><span data-stu-id="7745b-120">N</span></span>   | <span data-ttu-id="7745b-121">S</span><span class="sxs-lookup"><span data-stu-id="7745b-121">Y</span></span>        |
| <span data-ttu-id="7745b-122">ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="7745b-122">ReserveLocal</span></span>  | [<span data-ttu-id="7745b-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7745b-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7745b-124">N</span><span class="sxs-lookup"><span data-stu-id="7745b-124">N</span></span>   | <span data-ttu-id="7745b-125">N</span><span class="sxs-lookup"><span data-stu-id="7745b-125">N</span></span>        |
| <span data-ttu-id="7745b-126">ReserveSource</span><span class="sxs-lookup"><span data-stu-id="7745b-126">ReserveSource</span></span> | [<span data-ttu-id="7745b-127">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7745b-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7745b-128">N</span><span class="sxs-lookup"><span data-stu-id="7745b-128">N</span></span>   | <span data-ttu-id="7745b-129">N</span><span class="sxs-lookup"><span data-stu-id="7745b-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7745b-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="7745b-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7745b-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span><span class="sxs-lookup"><span data-stu-id="7745b-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="7745b-132">Chiave primaria che identifica in modo univoco una voce della tabella ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="7745b-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="7745b-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="7745b-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="7745b-134">Chiave esterna per la colonna uno della tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7745b-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="7745b-135">Riserva una quantità di spazio specificata se il componente deve essere installato.</span><span class="sxs-lookup"><span data-stu-id="7745b-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="7745b-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="7745b-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="7745b-137">Questa colonna contiene il nome di una proprietà che rappresenta il percorso completo della directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7745b-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="7745b-138">Questo nome di proprietà è in genere il nome di una directory nella tabella di [directory](directory-table.md) o il nome di un set di proprietà ottenuto utilizzando l'azione [AppSearch](appsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7745b-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="7745b-139">In questo modo viene aggiunta la quantità di spazio su disco specificata in ReserveLocal o ReserveSource al costo del volume del dispositivo che contiene la directory.</span><span class="sxs-lookup"><span data-stu-id="7745b-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="7745b-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="7745b-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="7745b-141">Numero di byte di spazio su disco da riservare se il componente collegato è installato per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="7745b-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="7745b-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span><span class="sxs-lookup"><span data-stu-id="7745b-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="7745b-143">Numero di byte di spazio su disco da riservare se il componente collegato è installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="7745b-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7745b-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="7745b-144">Remarks</span></span>

<span data-ttu-id="7745b-145">Il mantenimento dei costi in questo modo può essere utile per gli autori che desiderano garantire che una quantità minima di spazio su disco sarà disponibile al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="7745b-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="7745b-146">Questo spazio su disco, ad esempio, potrebbe essere riservato ai documenti utente o ai file dell'applicazione, ad esempio i file di indice, che vengono creati solo dopo l'avvio dell'applicazione dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="7745b-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="7745b-147">È possibile utilizzare la tabella ReserveCost per abilitare azioni personalizzate per specificare un costo approssimativo per tutti i file, le voci del registro di sistema o altri elementi che l'azione personalizzata potrebbe installare.</span><span class="sxs-lookup"><span data-stu-id="7745b-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="7745b-148">Le azioni personalizzate che aggiungono voci alla tabella ReserveCost devono essere sequenziate tra le azioni [CostInitialize](costinitialize-action.md) e [filecost](filecost-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7745b-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="7745b-149">Questa operazione è necessaria per l'azione filecost per inizializzare correttamente il costo di tutti i componenti interessati dalle voci nella tabella ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="7745b-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="7745b-150">Convalida</span><span class="sxs-lookup"><span data-stu-id="7745b-150">Validation</span></span>

<dl>

[<span data-ttu-id="7745b-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="7745b-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7745b-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="7745b-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7745b-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="7745b-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



