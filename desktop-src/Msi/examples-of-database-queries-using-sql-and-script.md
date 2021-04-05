---
description: Un esempio di utilizzo di query di database basate su script viene fornito in Windows Installer SDK (Software Development Kit) come WiRunSQL.vbs di utilità.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Esempi di query sul database con SQL e script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755626"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="5fda8-103">Esempi di query sul database con SQL e script</span><span class="sxs-lookup"><span data-stu-id="5fda8-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="5fda8-104">Un esempio di utilizzo di query di database basate su script è disponibile nel [Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) di Windows Installer come utilità WiRunSQL.vbs.</span><span class="sxs-lookup"><span data-stu-id="5fda8-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="5fda8-105">Questa utilità gestisce le query di database usando la versione Windows Installer di SQL descritta nella sezione [sintassi SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5fda8-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="5fda8-106">**Eliminare un record da una tabella**</span><span class="sxs-lookup"><span data-stu-id="5fda8-106">**Delete a record from a table**</span></span>

<span data-ttu-id="5fda8-107">La riga di comando seguente consente di eliminare il record con la chiave primaria rossa dalla tabella delle [funzionalità](feature-table.md) del database di Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="5fda8-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` feature \` Where \` feature \` . \` Feature \` = "rosso" "**</span><span class="sxs-lookup"><span data-stu-id="5fda8-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="5fda8-109">**Aggiungere una tabella a un database**</span><span class="sxs-lookup"><span data-stu-id="5fda8-109">**Add a table to a database**</span></span>

<span data-ttu-id="5fda8-110">La riga di comando seguente aggiunge la tabella di [directory](directory-table.md) al database Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="5fda8-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` directory \` ( \` directory \` char (72) not null, \` directory \_ Parent \` char (72), \` DefaultDir \` char (255) not null localizzable Primary Key \` directory \` )"**</span><span class="sxs-lookup"><span data-stu-id="5fda8-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="5fda8-112">**Rimuovere una tabella da un database**</span><span class="sxs-lookup"><span data-stu-id="5fda8-112">**Remove a table from a database**</span></span>

<span data-ttu-id="5fda8-113">La riga di comando seguente consente di rimuovere la tabella delle [funzionalità](feature-table.md) dal database Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="5fda8-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` feature \` "**</span><span class="sxs-lookup"><span data-stu-id="5fda8-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="5fda8-115">**Aggiungere una nuova colonna a una tabella**</span><span class="sxs-lookup"><span data-stu-id="5fda8-115">**Add a new column to a table**</span></span>

<span data-ttu-id="5fda8-116">La riga di comando seguente aggiunge la colonna di test alla tabella [CustomAction](customaction-table.md) del database di Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="5fda8-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` Add \` test \` Integer"**</span><span class="sxs-lookup"><span data-stu-id="5fda8-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="5fda8-118">**Inserire un nuovo record in una tabella**</span><span class="sxs-lookup"><span data-stu-id="5fda8-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="5fda8-119">Nella riga di comando seguente viene inserito un nuovo record nella tabella delle [funzionalità](feature-table.md) del database di Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="5fda8-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \` feature \` ( \` feature \` . \` Funzionalità \` \` \` . \` Funzionalità \_ \` , elemento \` padre \` . \` Titolo \` , \` funzionalità \` . \` Descrizione \` , \` funzionalità \` . \` Display \` , \` feature \` . \` Livello \` , \` funzionalità \` . \` Directory \_ \` , \` funzionalità \` . \` Attributi \` ) valori (' tennis ',' sport ',' tennis ',' Tournament ', 25, 3,' SPORTDIR ', 2) "**</span><span class="sxs-lookup"><span data-stu-id="5fda8-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="5fda8-121">Il record seguente viene inserito nella tabella delle [funzionalità](feature-table.md) di Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="5fda8-122">[Funzionalità](feature-table.md) di tavolo</span><span class="sxs-lookup"><span data-stu-id="5fda8-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="5fda8-123">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5fda8-123">Feature</span></span> | <span data-ttu-id="5fda8-124">\_Elemento padre della funzionalità</span><span class="sxs-lookup"><span data-stu-id="5fda8-124">Feature\_Parent</span></span> | <span data-ttu-id="5fda8-125">Titolo</span><span class="sxs-lookup"><span data-stu-id="5fda8-125">Title</span></span>  | <span data-ttu-id="5fda8-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fda8-126">Description</span></span> | <span data-ttu-id="5fda8-127">Visualizza</span><span class="sxs-lookup"><span data-stu-id="5fda8-127">Display</span></span> | <span data-ttu-id="5fda8-128">Level</span><span class="sxs-lookup"><span data-stu-id="5fda8-128">Level</span></span> | <span data-ttu-id="5fda8-129">Directory\_</span><span class="sxs-lookup"><span data-stu-id="5fda8-129">Directory\_</span></span> | <span data-ttu-id="5fda8-130">Attributi</span><span class="sxs-lookup"><span data-stu-id="5fda8-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="5fda8-131">Tennis</span><span class="sxs-lookup"><span data-stu-id="5fda8-131">Tennis</span></span>  | <span data-ttu-id="5fda8-132">Sport</span><span class="sxs-lookup"><span data-stu-id="5fda8-132">Sport</span></span>           | <span data-ttu-id="5fda8-133">Tennis</span><span class="sxs-lookup"><span data-stu-id="5fda8-133">Tennis</span></span> | <span data-ttu-id="5fda8-134">Tournament</span><span class="sxs-lookup"><span data-stu-id="5fda8-134">Tournament</span></span>  | <span data-ttu-id="5fda8-135">25</span><span class="sxs-lookup"><span data-stu-id="5fda8-135">25</span></span>      | <span data-ttu-id="5fda8-136">3</span><span class="sxs-lookup"><span data-stu-id="5fda8-136">3</span></span>     | <span data-ttu-id="5fda8-137">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="5fda8-137">SPORTDIR</span></span>    | <span data-ttu-id="5fda8-138">2</span><span class="sxs-lookup"><span data-stu-id="5fda8-138">2</span></span>          |



 

<span data-ttu-id="5fda8-139">Si noti che non è possibile inserire dati binari in una tabella usando direttamente le query INSERT INTO o UPDATE SQL.</span><span class="sxs-lookup"><span data-stu-id="5fda8-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="5fda8-140">Per informazioni, vedere [aggiunta di dati binari a una tabella con SQL](adding-binary-data-to-a-table-using-sql.md).</span><span class="sxs-lookup"><span data-stu-id="5fda8-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="5fda8-141">**Modificare un record esistente in una tabella**</span><span class="sxs-lookup"><span data-stu-id="5fda8-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="5fda8-142">La riga di comando seguente modifica il valore esistente nel campo title in "performances".</span><span class="sxs-lookup"><span data-stu-id="5fda8-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="5fda8-143">Il record aggiornato contiene "Arts" come chiave primaria ed è presente nella tabella delle funzionalità del database di Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="5fda8-144">**Cscript WiRunSQL.vbs Test.msi "aggiornare \` la \` funzionalità del set di funzionalità \` \` . \` Title \` = "performances" Where \` feature \` . \` Feature \` = "Arts" "**</span><span class="sxs-lookup"><span data-stu-id="5fda8-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="5fda8-145">**Seleziona un gruppo di record**</span><span class="sxs-lookup"><span data-stu-id="5fda8-145">**Select a group of records**</span></span>

<span data-ttu-id="5fda8-146">La riga di comando seguente consente di selezionare il nome e il tipo di tutti i controlli che appartengono a ErrorDialog nel database di Test.msi.</span><span class="sxs-lookup"><span data-stu-id="5fda8-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="5fda8-147">**CScript WiRunSQL.vbs Test.msi "selezionare il \` controllo \` , \` digitare \` da \` Control \` Where \` Dialog \_ \` =' ErrorDialog '"**</span><span class="sxs-lookup"><span data-stu-id="5fda8-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="5fda8-148">**Mantenere una tabella in memoria**</span><span class="sxs-lookup"><span data-stu-id="5fda8-148">**Hold a table in memory**</span></span>

<span data-ttu-id="5fda8-149">La riga di comando seguente blocca la tabella dei [componenti](component-table.md) del database Test.msi in memoria.</span><span class="sxs-lookup"><span data-stu-id="5fda8-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="5fda8-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` holding"**</span><span class="sxs-lookup"><span data-stu-id="5fda8-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="5fda8-151">**Liberare una tabella in memoria**</span><span class="sxs-lookup"><span data-stu-id="5fda8-151">**Free a table in memory**</span></span>

<span data-ttu-id="5fda8-152">La riga di comando seguente libera la tabella dei [componenti](component-table.md) del database Test.msi dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="5fda8-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="5fda8-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` Free"**</span><span class="sxs-lookup"><span data-stu-id="5fda8-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



