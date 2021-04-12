---
description: Le tabelle del gruppo tabelle di sistema tengono traccia delle tabelle e delle colonne del database di installazione.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Gruppo tabelle di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130270"
---
# <a name="system-tables-group"></a><span data-ttu-id="4ea56-103">Gruppo tabelle di sistema</span><span class="sxs-lookup"><span data-stu-id="4ea56-103">System Tables Group</span></span>

<span data-ttu-id="4ea56-104">Le tabelle del gruppo tabelle di sistema tengono traccia delle tabelle e delle colonne del database di installazione.</span><span class="sxs-lookup"><span data-stu-id="4ea56-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="4ea56-105">La [ \_ tabella](-tables-table.md) Tables tiene traccia di tutte le tabelle del database.</span><span class="sxs-lookup"><span data-stu-id="4ea56-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="4ea56-106">Sono incluse le tabelle che è possibile creare per le azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="4ea56-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="4ea56-107">Eseguire una query su questa tabella per verificare se esiste una tabella.</span><span class="sxs-lookup"><span data-stu-id="4ea56-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="4ea56-108">La [ \_ tabella Columns](-columns-table.md) tiene traccia delle colonne del database di installazione.</span><span class="sxs-lookup"><span data-stu-id="4ea56-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="4ea56-109">Attualmente le colonne temporanee non vengono rilevate da questa tabella.</span><span class="sxs-lookup"><span data-stu-id="4ea56-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="4ea56-110">Eseguire una query su questa tabella per determinare se esiste una determinata colonna.</span><span class="sxs-lookup"><span data-stu-id="4ea56-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="4ea56-111">La [ \_ tabella Streams](-streams-table.md) elenca i flussi di dati OLE incorporati.</span><span class="sxs-lookup"><span data-stu-id="4ea56-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="4ea56-112">La [ \_ tabella Storages](-storages-table.md) elenca le archiviazioni di dati OLE embedded.</span><span class="sxs-lookup"><span data-stu-id="4ea56-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="4ea56-113">[ \_ Tabella di convalida](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="4ea56-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="4ea56-114">La \_ tabella di convalida tiene traccia dei tipi e degli intervalli consentiti di ogni colonna nel database.</span><span class="sxs-lookup"><span data-stu-id="4ea56-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="4ea56-115">La \_ tabella di convalida viene utilizzata durante il processo di convalida del database per garantire che tutte le colonne siano contabilizzate e dispongano dei valori corretti.</span><span class="sxs-lookup"><span data-stu-id="4ea56-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="4ea56-116">Questa tabella non è inclusa nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="4ea56-116">This table is not shipped with the installer database.</span></span>

 

 



