---
description: La \_ tabella ForceCodepage è una tabella speciale utilizzata per modificare la tabella codici di un pacchetto di installazione. È possibile determinare o impostare la tabella codici esportando o importando un file di archivio di testo denominato \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311116"
---
# <a name="_forcecodepage"></a><span data-ttu-id="7f8a5-104">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="7f8a5-104">\_ForceCodepage</span></span>

<span data-ttu-id="7f8a5-105">La \_ tabella ForceCodepage è una tabella speciale utilizzata per modificare la tabella codici di un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="7f8a5-106">È possibile determinare o impostare la tabella codici esportando o importando un [file di archivio di testo](text-archive-files.md) denominato \_ ForceCodepage. IDT.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="7f8a5-107">Il formato della \_ tabella ForceCodepage è 2 righe vuote seguite da una terza riga che indica la tabella codici numerici.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="7f8a5-108">Ad esempio, un \_ file table. IDT di ForceCodepage per un database giapponese avrà un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="7f8a5-109">La tabella codici numerici in questo caso è 932.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="7f8a5-110">Per ulteriori informazioni sull'utilizzo di \_ ForceCodepage per ottenere o impostare la tabella codici di un database, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="7f8a5-111">Gestione della tabella codici (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="7f8a5-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="7f8a5-112">Determinazione della tabella codici di un database di installazione</span><span class="sxs-lookup"><span data-stu-id="7f8a5-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="7f8a5-113">Impostazione della tabella codici di un database</span><span class="sxs-lookup"><span data-stu-id="7f8a5-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="7f8a5-114">La \_ tabella ForceCodepage è una pseudo-tabella speciale utilizzata per modificare la tabella codici di un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="7f8a5-115">Utilizzando la \_ tabella ForceCodepage, il database viene impostato in modo incondizionato sulla tabella codici senza eseguire alcuna convalida per determinare se i dati attualmente presenti nel database possono essere convertiti nella nuova tabella codici.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="7f8a5-116">È sempre consigliabile che la modifica della tabella codici di un database inizi con un database indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="7f8a5-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



