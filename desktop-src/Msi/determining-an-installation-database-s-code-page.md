---
description: Per determinare la tabella codici di un database, chiamare MsiDatabaseExport con hDatabase impostato sull'handle del database e szTableName impostato su \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinazione della tabella codici di un database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882993"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="bf8f8-103">Determinazione della tabella codici di un database di installazione</span><span class="sxs-lookup"><span data-stu-id="bf8f8-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="bf8f8-104">Per determinare la tabella codici di un database, chiamare [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* impostato sull'handle del database e *szTableName* impostato su \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="bf8f8-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="bf8f8-105">Viene esportato un file di testo con estensione IDT.</span><span class="sxs-lookup"><span data-stu-id="bf8f8-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="bf8f8-106">Le prime due righe del file sono vuote.</span><span class="sxs-lookup"><span data-stu-id="bf8f8-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="bf8f8-107">La terza riga è il numero di tabella codici ANSI, seguito da una scheda, seguito dal nome \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="bf8f8-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="bf8f8-108">Vedere anche [gestione della tabella codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bf8f8-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="bf8f8-109">Un esempio di determinazione della tabella codici tramite il [**Metodo Export**](database-export.md) viene fornito nel Windows Installer SDK come parte del WiLangId.vbs di utilità.</span><span class="sxs-lookup"><span data-stu-id="bf8f8-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="bf8f8-110">Per ulteriori informazioni sull'utilizzo di WiLangId.vbs, vedere l'argomento relativo alla [gestione della lingua e](manage-language-and-codepage.md)della tabella codici.</span><span class="sxs-lookup"><span data-stu-id="bf8f8-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



