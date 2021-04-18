---
description: Una specifica dell'esempio è che le informazioni dell'account utente vengono lette da una tabella personalizzata nel database di installazione e non sono hardcoded nell'azione personalizzata.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Aggiunta di una tabella CustomUserAccounts personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311084"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="a9b4a-103">Aggiunta di una tabella CustomUserAccounts personalizzata</span><span class="sxs-lookup"><span data-stu-id="a9b4a-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="a9b4a-104">Una specifica dell'esempio è che le informazioni dell'account utente vengono lette da una tabella personalizzata nel database di installazione e non sono hardcoded nell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="a9b4a-105">Aggiungere una tabella personalizzata al database di installazione di esempio denominato CustomUserAccounts per conservare le informazioni dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="a9b4a-106">Per un esempio di come aggiungere una tabella personalizzata, vedere [esempi di query sul database con SQL e script](examples-of-database-queries-using-sql-and-script.md) .</span><span class="sxs-lookup"><span data-stu-id="a9b4a-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="a9b4a-107">Utilizzare lo schema seguente per la tabella CustomUserAccounts.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="a9b4a-108">Per una spiegazione dei tipi di colonna, vedere [formato della definizione di colonna](column-definition-format.md) .</span><span class="sxs-lookup"><span data-stu-id="a9b4a-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="a9b4a-109">Colonna</span><span class="sxs-lookup"><span data-stu-id="a9b4a-109">Column</span></span>     | <span data-ttu-id="a9b4a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9b4a-110">Type</span></span> | <span data-ttu-id="a9b4a-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="a9b4a-111">Key</span></span> | <span data-ttu-id="a9b4a-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="a9b4a-112">Nullable</span></span> | <span data-ttu-id="a9b4a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9b4a-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b4a-114">UserName</span><span class="sxs-lookup"><span data-stu-id="a9b4a-114">UserName</span></span>   | <span data-ttu-id="a9b4a-115">S72</span><span class="sxs-lookup"><span data-stu-id="a9b4a-115">s72</span></span>  | <span data-ttu-id="a9b4a-116">S</span><span class="sxs-lookup"><span data-stu-id="a9b4a-116">Y</span></span>   | <span data-ttu-id="a9b4a-117">N</span><span class="sxs-lookup"><span data-stu-id="a9b4a-117">N</span></span>        | <span data-ttu-id="a9b4a-118">Nome dell'account utente in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a9b4a-119">Password</span><span class="sxs-lookup"><span data-stu-id="a9b4a-119">Password</span></span>   | <span data-ttu-id="a9b4a-120">S72</span><span class="sxs-lookup"><span data-stu-id="a9b4a-120">s72</span></span>  |     | <span data-ttu-id="a9b4a-121">N</span><span class="sxs-lookup"><span data-stu-id="a9b4a-121">N</span></span>        | <span data-ttu-id="a9b4a-122">Nome della proprietà contenente la password per l'account.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="a9b4a-123">Si tratta di una [proprietà pubblica](public-properties.md) impostata nella riga di comando o tramite un [controllo di modifica](edit-control.md) nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="a9b4a-124">Questo controllo di modifica deve avere l' [attributo di controllo password](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a9b4a-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="a9b4a-125">Attributi</span><span class="sxs-lookup"><span data-stu-id="a9b4a-125">Attributes</span></span> | <span data-ttu-id="a9b4a-126">i4</span><span class="sxs-lookup"><span data-stu-id="a9b4a-126">i4</span></span>   |     | <span data-ttu-id="a9b4a-127">S</span><span class="sxs-lookup"><span data-stu-id="a9b4a-127">Y</span></span>        | <span data-ttu-id="a9b4a-128">Attributi per l'account.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-128">Attributes for account.</span></span> <span data-ttu-id="a9b4a-129">Questi vengono definiti come valori **DWORD** per il \_ membro dei flag usri1 della struttura di \_ informazioni utente \_ 1.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="a9b4a-130">Dopo che la tabella CustomUserAccounts è stata aggiunta al database, è possibile modificare la tabella usando Orca, un editor di tabelle fornito con Windows Installer SDK o un altro editor.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="a9b4a-131">Immettere il record seguente nella tabella CustomUserAccounts per creare un account utente protetto da password per un utente denominato TestUser.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="a9b4a-132">Si noti che 512 è il valore numerico per \_ l' \_ account UF Normal.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="a9b4a-133">Tabella CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a9b4a-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="a9b4a-134">UserName</span><span class="sxs-lookup"><span data-stu-id="a9b4a-134">UserName</span></span> | <span data-ttu-id="a9b4a-135">Password</span><span class="sxs-lookup"><span data-stu-id="a9b4a-135">Password</span></span>         | <span data-ttu-id="a9b4a-136">Attributi</span><span class="sxs-lookup"><span data-stu-id="a9b4a-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="a9b4a-137">TestUser</span><span class="sxs-lookup"><span data-stu-id="a9b4a-137">TestUser</span></span> | <span data-ttu-id="a9b4a-138">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="a9b4a-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="a9b4a-139">512</span><span class="sxs-lookup"><span data-stu-id="a9b4a-139">512</span></span>        |



 

<span data-ttu-id="a9b4a-140">Aggiungere i record seguenti alla \_ tabella di convalida per la tabella personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a9b4a-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="a9b4a-141">\_Tabella di convalida</span><span class="sxs-lookup"><span data-stu-id="a9b4a-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="a9b4a-142">Tabella</span><span class="sxs-lookup"><span data-stu-id="a9b4a-142">Table</span></span>              | <span data-ttu-id="a9b4a-143">Colonna</span><span class="sxs-lookup"><span data-stu-id="a9b4a-143">Column</span></span>     | <span data-ttu-id="a9b4a-144">Nullable</span><span class="sxs-lookup"><span data-stu-id="a9b4a-144">Nullable</span></span> | <span data-ttu-id="a9b4a-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="a9b4a-145">MinValue</span></span> | <span data-ttu-id="a9b4a-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a9b4a-146">MaxValue</span></span>   | <span data-ttu-id="a9b4a-147">KeyTable</span><span class="sxs-lookup"><span data-stu-id="a9b4a-147">KeyTable</span></span> | <span data-ttu-id="a9b4a-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="a9b4a-148">KeyColumn</span></span> | <span data-ttu-id="a9b4a-149">Category</span><span class="sxs-lookup"><span data-stu-id="a9b4a-149">Category</span></span>                     | <span data-ttu-id="a9b4a-150">Set</span><span class="sxs-lookup"><span data-stu-id="a9b4a-150">Set</span></span> | <span data-ttu-id="a9b4a-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9b4a-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="a9b4a-152">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a9b4a-152">CustomUserAccounts</span></span> | <span data-ttu-id="a9b4a-153">UserName</span><span class="sxs-lookup"><span data-stu-id="a9b4a-153">UserName</span></span>   | <span data-ttu-id="a9b4a-154">N</span><span class="sxs-lookup"><span data-stu-id="a9b4a-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="a9b4a-155">Text</span><span class="sxs-lookup"><span data-stu-id="a9b4a-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="a9b4a-156">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a9b4a-156">CustomUserAccounts</span></span> | <span data-ttu-id="a9b4a-157">Password</span><span class="sxs-lookup"><span data-stu-id="a9b4a-157">Password</span></span>   | <span data-ttu-id="a9b4a-158">N</span><span class="sxs-lookup"><span data-stu-id="a9b4a-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="a9b4a-159">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a9b4a-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="a9b4a-160">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a9b4a-160">CustomUserAccounts</span></span> | <span data-ttu-id="a9b4a-161">Attributi</span><span class="sxs-lookup"><span data-stu-id="a9b4a-161">Attributes</span></span> | <span data-ttu-id="a9b4a-162">S</span><span class="sxs-lookup"><span data-stu-id="a9b4a-162">Y</span></span>        | <span data-ttu-id="a9b4a-163">0</span><span class="sxs-lookup"><span data-stu-id="a9b4a-163">0</span></span>        | <span data-ttu-id="a9b4a-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="a9b4a-164">2147483647</span></span> |          |           | <span data-ttu-id="a9b4a-165">Null</span><span class="sxs-lookup"><span data-stu-id="a9b4a-165">null</span></span>                         |     |             |



 

<span data-ttu-id="a9b4a-166">Continuare a [creare le tabelle ActionText e Error](authoring-the-actiontext-and-error-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a9b4a-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



