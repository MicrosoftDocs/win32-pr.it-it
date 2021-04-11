---
description: È possibile utilizzare il programma di installazione per importare un archivio di testo in un database attivo, nonché per esportare un file di database in un archivio di testo. Questa operazione può essere utile per i sistemi di controllo del codice sorgente basati su testo.
ms.assetid: 1025da16-9e1f-4fb4-9ce1-f992970eb903
title: Importazione ed esportazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb778f4a0fe415686c80f2609f63958ae042d920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130446"
---
# <a name="importing-and-exporting"></a><span data-ttu-id="dd119-104">Importazione ed esportazione</span><span class="sxs-lookup"><span data-stu-id="dd119-104">Importing and Exporting</span></span>

<span data-ttu-id="dd119-105">È possibile utilizzare il programma di installazione per importare un archivio di testo in un database attivo, nonché per esportare un file di database in un archivio di testo.</span><span class="sxs-lookup"><span data-stu-id="dd119-105">You can use the installer to import a text archive into an active database as well as to export a database file to a text archive.</span></span> <span data-ttu-id="dd119-106">Questa operazione può essere utile per i sistemi di controllo del codice sorgente basati su testo.</span><span class="sxs-lookup"><span data-stu-id="dd119-106">This can be useful for text-based source control systems.</span></span>

<span data-ttu-id="dd119-107">Per importare un archivio di testo in un database attivo, chiamare la funzione [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .</span><span class="sxs-lookup"><span data-stu-id="dd119-107">To import a text archive into an active database, call the [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) function.</span></span>

<span data-ttu-id="dd119-108">Per esportare un file di database in un archivio di testo, chiamare la funzione [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) .</span><span class="sxs-lookup"><span data-stu-id="dd119-108">To export a database file to a text archive, call the [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) function.</span></span>

 

 



