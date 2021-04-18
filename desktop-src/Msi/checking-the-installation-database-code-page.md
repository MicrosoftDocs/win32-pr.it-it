---
description: Una tabella codici è una tabella interna utilizzata dal sistema operativo per eseguire il mapping dei simboli (lettere, numeri e segni di punteggiatura) a un numero di caratteri.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Controllo della tabella codici del database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310985"
---
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="566b3-103">Controllo della tabella codici del database di installazione</span><span class="sxs-lookup"><span data-stu-id="566b3-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="566b3-104">Una tabella *codici* è una tabella interna utilizzata dal sistema operativo per eseguire il mapping dei simboli (lettere, numeri e segni di punteggiatura) a un numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="566b3-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="566b3-105">Diverse tabelle codici forniscono supporto per i set di caratteri utilizzati in diversi paesi o aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="566b3-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="566b3-106">Alle tabelle codici viene fatto riferimento in base al numero; ad esempio, la tabella codici 932 rappresenta il set di caratteri giapponese e la tabella codici 950 rappresenta uno dei set di caratteri cinesi.</span><span class="sxs-lookup"><span data-stu-id="566b3-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="566b3-107">Vedere [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md) per un elenco di tabelle codici ASCII.</span><span class="sxs-lookup"><span data-stu-id="566b3-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="566b3-108">La stessa tabella codici ASCII, 1252, può essere utilizzata per l'inglese e il francese.</span><span class="sxs-lookup"><span data-stu-id="566b3-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="566b3-109">Pertanto, non è necessario reimpostare la tabella codici per il database MNP2000.msi (Inglese) per modificare l'installazione in francese.</span><span class="sxs-lookup"><span data-stu-id="566b3-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="566b3-110">Per ulteriori informazioni sull'impostazione della tabella codici, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="566b3-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="566b3-111">Continua</span><span class="sxs-lookup"><span data-stu-id="566b3-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



