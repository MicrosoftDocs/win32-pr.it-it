---
description: Rappresentano i tipi per i database di shim principale e personalizzati.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipi di database shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747674"
---
# <a name="shim-database-types"></a><span data-ttu-id="cea04-103">Tipi di database shim</span><span class="sxs-lookup"><span data-stu-id="cea04-103">Shim Database Types</span></span>

<span data-ttu-id="cea04-104">Rappresentano i tipi per i database di shim principale e personalizzati.</span><span class="sxs-lookup"><span data-stu-id="cea04-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="cea04-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="cea04-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="cea04-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cea04-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="cea04-107"><dt>**Sdb \_ 0x80000000 \_ principale database**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cea04-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="cea04-108">Database principale.</span><span class="sxs-lookup"><span data-stu-id="cea04-108">The main database.</span></span> <span data-ttu-id="cea04-109">Se questo flag non è presente, il database è un database personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cea04-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="cea04-110"><dt>**Sdb \_ 0x00010000 \_ shim database**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cea04-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="cea04-111">Il database contiene le voci dell'applicazione da sottoposto a shim.</span><span class="sxs-lookup"><span data-stu-id="cea04-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="cea04-112"><dt>**Sdb \_ 0x00020000 \_ MSI del database**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cea04-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="cea04-113">Il database contiene voci MSI.</span><span class="sxs-lookup"><span data-stu-id="cea04-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="cea04-114"><dt>**Sdb \_ \_Driver di database**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="cea04-115">Il database contiene voci di blocco del driver.</span><span class="sxs-lookup"><span data-stu-id="cea04-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="cea04-116"><dt>**Sdb \_ \_Dettagli database**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="cea04-117">Il database contiene i dettagli apphelp.</span><span class="sxs-lookup"><span data-stu-id="cea04-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="cea04-118"><dt>**Sdb \_ \_ \_ Dettagli SP database**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="cea04-119">Il database contiene i dettagli di SP apphelp.</span><span class="sxs-lookup"><span data-stu-id="cea04-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="cea04-120"><dt>**Sdb \_ 0x00200000 \_ risorsa database**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cea04-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="cea04-121">La DLL della risorsa contiene i dettagli apphelp.</span><span class="sxs-lookup"><span data-stu-id="cea04-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="cea04-122"><dt>**Sdb \_ \_ \_ Maschera del tipo di database**</dt> <dt>0xF02F0000</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="cea04-123">Maschera utilizzata per estrarre le informazioni sul database principale.</span><span class="sxs-lookup"><span data-stu-id="cea04-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="cea04-124"><dt>**\_ \_ shim principale del database sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="cea04-125">Metodo SDB database shim SDB database MSI SDB database \_ \_ \| \_ \_ \| \_ \_ principale</span><span class="sxs-lookup"><span data-stu-id="cea04-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="cea04-126"><dt>**\_ \_ MSI principale del database sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="cea04-127">database \_ sdb \_ MSI \| sdb \_ database \_ Main</span><span class="sxs-lookup"><span data-stu-id="cea04-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="cea04-128"><dt>**\_ \_ driver principali del database sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="cea04-129">\_driver di database sdb \_ \| sdb \_ database \_ Main</span><span class="sxs-lookup"><span data-stu-id="cea04-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="cea04-130"><dt>**\_ \_ Dettagli principale del database sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="cea04-131">informazioni di base sul \_ database sdb \_ \| sdb \_ database \_ Main</span><span class="sxs-lookup"><span data-stu-id="cea04-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="cea04-132"><dt>**\_ \_ \_ Dettagli SP principale del database sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="cea04-133">\_database sdb \_ Dettagli SP database \_ \| sdb \_ \_ principale</span><span class="sxs-lookup"><span data-stu-id="cea04-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="cea04-134"><dt>**\_ \_ risorsa principale del database sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="cea04-135">risorsa del database sdb \_ \_ \| sdb \_ database \_ Main</span><span class="sxs-lookup"><span data-stu-id="cea04-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="cea04-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cea04-136">Requirements</span></span>



| <span data-ttu-id="cea04-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea04-137">Requirement</span></span> | <span data-ttu-id="cea04-138">Valore</span><span class="sxs-lookup"><span data-stu-id="cea04-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cea04-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cea04-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cea04-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cea04-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cea04-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cea04-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cea04-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cea04-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cea04-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cea04-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea04-144">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="cea04-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




