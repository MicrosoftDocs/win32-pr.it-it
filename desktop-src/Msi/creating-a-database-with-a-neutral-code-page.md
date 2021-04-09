---
description: L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database di base neutro che contenga solo caratteri che possono essere convertiti in qualsiasi tabella codici.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Creazione di un database con una tabella codici neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050160"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a><span data-ttu-id="2e7cd-103">Creazione di un database con una tabella codici neutra</span><span class="sxs-lookup"><span data-stu-id="2e7cd-103">Creating a Database with a Neutral Code Page</span></span>

<span data-ttu-id="2e7cd-104">L'approccio consigliato per la gestione delle tabelle codici consiste nel creare un database di base neutro che contenga solo caratteri che possono essere convertiti in qualsiasi tabella codici.</span><span class="sxs-lookup"><span data-stu-id="2e7cd-104">The recommended approach for handling code pages is to author a neutral base database that only contains characters that can be translated into any code page.</span></span> <span data-ttu-id="2e7cd-105">Il database può quindi essere impostato sulla tabella codici della localizzazione e le informazioni di localizzazione possono essere aggiunte come descritto in [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="2e7cd-105">The database may then be set to the code page of the localization and the localization information can be added as described in [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="2e7cd-106">Per creare un database neutro, evitare i caratteri estesi che non appartengono al set di caratteri ASCII e quindi richiedere una tabella codici speciale.</span><span class="sxs-lookup"><span data-stu-id="2e7cd-106">To author a neutral database, avoid extended characters that do not belong to the ASCII character set and therefore require a special code page.</span></span> <span data-ttu-id="2e7cd-107">Ad esempio, il segno di copyright, il © e il segno di marchio registrato,, non sono caratteri ASCII e richiedono una tabella codici ANSI speciale per la visualizzazione corretta.</span><span class="sxs-lookup"><span data-stu-id="2e7cd-107">For example, the copyright sign, ©, and the registered trademark sign, , are not ASCII characters, and require a special ANSI code page for proper display.</span></span> <span data-ttu-id="2e7cd-108">Usare invece (c) e (r), perché questi caratteri possono essere convertiti o trasformati in simboli per la versione in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="2e7cd-108">Instead use (c) and (r), because these characters can be translated or transformed to the symbols for the English-language version.</span></span> <span data-ttu-id="2e7cd-109">Questo database neutro può quindi essere localizzato impostando la relativa tabella codici e aggiungendo le informazioni di localizzazione mediante la modifica della tabella oppure importando i file di archivio di testo.</span><span class="sxs-lookup"><span data-stu-id="2e7cd-109">This neutral database can then be localized by setting its code page and adding localization information by table editing or by importing text archive files.</span></span>

 

 



