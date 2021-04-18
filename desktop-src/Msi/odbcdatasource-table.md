---
description: Nella tabella ODBCDataSource sono elencate le origini dati appartenenti all'installazione.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabella ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308179"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="2c4d6-103">Tabella ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="2c4d6-103">ODBCDataSource Table</span></span>

<span data-ttu-id="2c4d6-104">Nella tabella ODBCDataSource sono elencate le origini dati appartenenti all'installazione.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="2c4d6-105">La tabella ODBCDataSource include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="2c4d6-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="2c4d6-106">Column</span></span>            | <span data-ttu-id="2c4d6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c4d6-107">Type</span></span>                         | <span data-ttu-id="2c4d6-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="2c4d6-108">Key</span></span> | <span data-ttu-id="2c4d6-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2c4d6-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="2c4d6-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="2c4d6-110">DataSource</span></span>        | [<span data-ttu-id="2c4d6-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="2c4d6-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2c4d6-112">S</span><span class="sxs-lookup"><span data-stu-id="2c4d6-112">Y</span></span>   | <span data-ttu-id="2c4d6-113">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-113">N</span></span>        |
| <span data-ttu-id="2c4d6-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="2c4d6-114">Component\_</span></span>       | [<span data-ttu-id="2c4d6-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="2c4d6-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="2c4d6-116">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-116">N</span></span>   | <span data-ttu-id="2c4d6-117">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-117">N</span></span>        |
| <span data-ttu-id="2c4d6-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c4d6-118">Description</span></span>       | [<span data-ttu-id="2c4d6-119">Text</span><span class="sxs-lookup"><span data-stu-id="2c4d6-119">Text</span></span>](text.md)             | <span data-ttu-id="2c4d6-120">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-120">N</span></span>   | <span data-ttu-id="2c4d6-121">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-121">N</span></span>        |
| <span data-ttu-id="2c4d6-122">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="2c4d6-122">DriverDescription</span></span> | [<span data-ttu-id="2c4d6-123">Text</span><span class="sxs-lookup"><span data-stu-id="2c4d6-123">Text</span></span>](text.md)             | <span data-ttu-id="2c4d6-124">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-124">N</span></span>   | <span data-ttu-id="2c4d6-125">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-125">N</span></span>        |
| <span data-ttu-id="2c4d6-126">Registrazione</span><span class="sxs-lookup"><span data-stu-id="2c4d6-126">Registration</span></span>      | [<span data-ttu-id="2c4d6-127">Integer</span><span class="sxs-lookup"><span data-stu-id="2c4d6-127">Integer</span></span>](integer.md)       | <span data-ttu-id="2c4d6-128">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-128">N</span></span>   | <span data-ttu-id="2c4d6-129">N</span><span class="sxs-lookup"><span data-stu-id="2c4d6-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2c4d6-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="2c4d6-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2c4d6-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span><span class="sxs-lookup"><span data-stu-id="2c4d6-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="2c4d6-132">Nome del token interno per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-132">Internal token name for data source.</span></span> <span data-ttu-id="2c4d6-133">Chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="2c4d6-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="2c4d6-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2c4d6-135">Chiave esterna nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="2c4d6-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c4d6-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c4d6-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="2c4d6-137">Descrizione registrata per questa origine dati.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-137">The description registered for this data source.</span></span> <span data-ttu-id="2c4d6-138">Questo valore non può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-138">This value cannot be localized.</span></span> <span data-ttu-id="2c4d6-139">Le descrizioni delle origini dati ODBC non possono superare la \_ lunghezza massima del \_ DSN SQL \_ .</span><span class="sxs-lookup"><span data-stu-id="2c4d6-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="2c4d6-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span><span class="sxs-lookup"><span data-stu-id="2c4d6-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="2c4d6-141">Driver associato che può essere preesistente.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="2c4d6-142">Questo valore non può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="2c4d6-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registrazione</span><span class="sxs-lookup"><span data-stu-id="2c4d6-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="2c4d6-144">Questo campo specifica il tipo di registrazione per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="2c4d6-145">Costante</span><span class="sxs-lookup"><span data-stu-id="2c4d6-145">Constant</span></span>                                      | <span data-ttu-id="2c4d6-146">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="2c4d6-146">Hexadecimal</span></span> | <span data-ttu-id="2c4d6-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="2c4d6-147">Decimal</span></span> | <span data-ttu-id="2c4d6-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c4d6-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="2c4d6-149">**msidbODBCDataSourceRegistrationPerMachine**</span><span class="sxs-lookup"><span data-stu-id="2c4d6-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="2c4d6-150">0x000</span><span class="sxs-lookup"><span data-stu-id="2c4d6-150">0x000</span></span>       | <span data-ttu-id="2c4d6-151">0</span><span class="sxs-lookup"><span data-stu-id="2c4d6-151">0</span></span>       | <span data-ttu-id="2c4d6-152">L'origine dati è registrata per computer.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="2c4d6-153">**msidbODBCDataSourceRegistrationPerUser**</span><span class="sxs-lookup"><span data-stu-id="2c4d6-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="2c4d6-154">0x001</span><span class="sxs-lookup"><span data-stu-id="2c4d6-154">0x001</span></span>       | <span data-ttu-id="2c4d6-155">1</span><span class="sxs-lookup"><span data-stu-id="2c4d6-155">1</span></span>       | <span data-ttu-id="2c4d6-156">L'origine dati è registrata per utente.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c4d6-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c4d6-157">Remarks</span></span>

<span data-ttu-id="2c4d6-158">Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="2c4d6-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="2c4d6-159">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2c4d6-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="2c4d6-160">Convalida</span><span class="sxs-lookup"><span data-stu-id="2c4d6-160">Validation</span></span>

<dl>

[<span data-ttu-id="2c4d6-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="2c4d6-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2c4d6-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="2c4d6-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2c4d6-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="2c4d6-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2c4d6-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="2c4d6-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="2c4d6-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="2c4d6-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



