---
description: Windows 7 introduce le librerie, che offrono agli utenti un'unica visualizzazione coerente dei file, anche quando tali file sono archiviati in percorsi diversi.
title: Librerie di Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980935"
---
# <a name="windows-libraries"></a><span data-ttu-id="fac95-103">Librerie di Windows</span><span class="sxs-lookup"><span data-stu-id="fac95-103">Windows Libraries</span></span>

<span data-ttu-id="fac95-104">Windows 7 introduce le librerie, che offrono agli utenti un'unica visualizzazione coerente dei file, anche quando tali file sono archiviati in percorsi diversi.</span><span class="sxs-lookup"><span data-stu-id="fac95-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="fac95-105">Le librerie possono essere configurate e organizzate da un utente e una raccolta può contenere cartelle trovate nel computer dell'utente e anche cartelle condivise in rete.</span><span class="sxs-lookup"><span data-stu-id="fac95-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="fac95-106">Le librerie presentano una visualizzazione più semplice del sistema di archiviazione sottostante perché, per l'utente, i file e le cartelle in una raccolta vengono visualizzati in una singola visualizzazione, indipendentemente dalla posizione in cui sono archiviati fisicamente.</span><span class="sxs-lookup"><span data-stu-id="fac95-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="fac95-107">Gli sviluppatori che scrivono nuovi programmi in Windows 7 sono invitati a usare le librerie come mezzo tramite cui gli utenti interagiscono con i file usati dal programma.</span><span class="sxs-lookup"><span data-stu-id="fac95-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="fac95-108">L'utilizzo delle librerie nel programma fornirà agli utenti un'esperienza più semplice e intuitiva in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fac95-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="fac95-109">Gli sviluppatori devono anche esaminare i programmi esistenti e aggiornarli, se necessario, per lavorare con le librerie.</span><span class="sxs-lookup"><span data-stu-id="fac95-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="fac95-110">Poiché le librerie non fanno parte del file system, le API basate su file system non avranno accesso alle librerie che l'utente potrebbe avere configurato.</span><span class="sxs-lookup"><span data-stu-id="fac95-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="fac95-111">I programmi che attualmente consentono agli utenti di archiviare il contenuto in cartelle diverse o in computer diversi trarranno maggiore vantaggio quando aggiungono il supporto per le librerie.</span><span class="sxs-lookup"><span data-stu-id="fac95-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="fac95-112">Le librerie semplificano la gestione del contenuto in diverse posizioni di archiviazione per lo sviluppatore e l'utente.</span><span class="sxs-lookup"><span data-stu-id="fac95-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="fac95-113">In questa guida vengono descritte le librerie, il modo in cui è possibile eseguire i programmi per lavorare con le librerie e alcuni dei modi in cui un programma può utilizzare le librerie per migliorare l'esperienza dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fac95-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fac95-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fac95-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac95-115">Informazioni sulle librerie</span><span class="sxs-lookup"><span data-stu-id="fac95-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="fac95-116">Uso delle librerie nel programma</span><span class="sxs-lookup"><span data-stu-id="fac95-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="fac95-117">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="fac95-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="fac95-118">Collegamenti Shell</span><span class="sxs-lookup"><span data-stu-id="fac95-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="fac95-119">Cartelle note</span><span class="sxs-lookup"><span data-stu-id="fac95-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="fac95-120">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="fac95-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
