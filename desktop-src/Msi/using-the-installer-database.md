---
description: Il database del programma di installazione consente allo sviluppatore di un pacchetto di installazione di controllare il trasferimento di un'applicazione da un'origine a un'immagine di destinazione.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Utilizzo del database del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312312"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="7df7e-103">Utilizzo del database del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="7df7e-103">Using the Installer Database</span></span>

<span data-ttu-id="7df7e-104">Il [database del programma](installer-database.md) di installazione consente allo sviluppatore di un pacchetto di installazione di controllare il trasferimento di un'applicazione da un'origine a un'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7df7e-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="7df7e-105">Il layout delle immagini di origine e di destinazione dell'applicazione viene specificato nella tabella di [directory](directory-table.md) e le azioni che installano l'applicazione vengono specificate in sei tabelle di sequenza:</span><span class="sxs-lookup"><span data-stu-id="7df7e-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="7df7e-106">Tabella [InstallUISequence](installuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="7df7e-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="7df7e-107">Tabella [InstallExecuteSequence](installexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="7df7e-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="7df7e-108">Tabella [AdminUISequence](adminuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="7df7e-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="7df7e-109">Tabella [AdminExecuteSequence](adminexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="7df7e-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="7df7e-110">Tabella [AdvtUISequence](advtuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="7df7e-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="7df7e-111">Tabella [AdvtExecuteSequence](advtexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="7df7e-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="7df7e-112">Le sezioni seguenti descrivono come usare il [database del programma di installazione](installer-database.md):</span><span class="sxs-lookup"><span data-stu-id="7df7e-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="7df7e-113">Uso della tabella di directory</span><span class="sxs-lookup"><span data-stu-id="7df7e-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="7df7e-114">Utilizzo di una tabella di sequenza</span><span class="sxs-lookup"><span data-stu-id="7df7e-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="7df7e-115">Acquisizione di un handle di database</span><span class="sxs-lookup"><span data-stu-id="7df7e-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="7df7e-116">Commit dei database</span><span class="sxs-lookup"><span data-stu-id="7df7e-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="7df7e-117">Importazione ed esportazione</span><span class="sxs-lookup"><span data-stu-id="7df7e-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="7df7e-118">Unione di database</span><span class="sxs-lookup"><span data-stu-id="7df7e-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="7df7e-119">Denominazione di tabelle, proprietà e azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="7df7e-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="7df7e-120">Limitazioni OLE sui flussi</span><span class="sxs-lookup"><span data-stu-id="7df7e-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="7df7e-121">Utilizzo delle query</span><span class="sxs-lookup"><span data-stu-id="7df7e-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="7df7e-122">Aggiunta di dati binari a una tabella tramite SQL</span><span class="sxs-lookup"><span data-stu-id="7df7e-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="7df7e-123">Utilizzo dei record</span><span class="sxs-lookup"><span data-stu-id="7df7e-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="7df7e-124">Uso dei percorsi delle cartelle</span><span class="sxs-lookup"><span data-stu-id="7df7e-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="7df7e-125">Specifica dell'ordine di registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="7df7e-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="7df7e-126">Esecuzione delle azioni di condizionamento durante la rimozione</span><span class="sxs-lookup"><span data-stu-id="7df7e-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="7df7e-127">Chiamata di funzioni di database da programmi</span><span class="sxs-lookup"><span data-stu-id="7df7e-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="7df7e-128">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="7df7e-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="7df7e-129">Formato della definizione di colonna</span><span class="sxs-lookup"><span data-stu-id="7df7e-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="7df7e-130">Determinare se una colonna è una chiave primaria o esterna</span><span class="sxs-lookup"><span data-stu-id="7df7e-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



