---
description: Le categorie consentono di organizzare gli eventi in modo che Visualizzatore eventi possibile filtrarli. Ogni origine evento può definire le proprie categorie numerate e le stringhe di testo a cui viene eseguito il mapping.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorie di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308374"
---
# <a name="event-categories"></a><span data-ttu-id="54dde-104">Categorie di eventi</span><span class="sxs-lookup"><span data-stu-id="54dde-104">Event Categories</span></span>

<span data-ttu-id="54dde-105">Le categorie consentono di organizzare gli eventi in modo che Visualizzatore eventi possibile filtrarli.</span><span class="sxs-lookup"><span data-stu-id="54dde-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="54dde-106">Ogni [origine evento](event-sources.md) può definire le proprie categorie numerate e le stringhe di testo a cui viene eseguito il mapping.</span><span class="sxs-lookup"><span data-stu-id="54dde-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="54dde-107">Le categorie devono essere numerate consecutivamente, a partire dal numero 1.</span><span class="sxs-lookup"><span data-stu-id="54dde-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="54dde-108">Le categorie stesse sono definite in un file di messaggio.</span><span class="sxs-lookup"><span data-stu-id="54dde-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="54dde-109">Usare, ad esempio, la sintassi seguente per dichiarare tre categorie di eventi.</span><span class="sxs-lookup"><span data-stu-id="54dde-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="54dde-110">In Visualizzatore eventi, gli eventi che utilizzano queste categorie avranno la categoria 1, categoria 2 o la categoria 3 visualizzata nella colonna **categoria** .</span><span class="sxs-lookup"><span data-stu-id="54dde-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

<span data-ttu-id="54dde-111">Le categorie possono essere archiviate in un file di messaggi separato o in un file che contiene messaggi di altri tipi.</span><span class="sxs-lookup"><span data-stu-id="54dde-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="54dde-112">Se si crea un singolo file di messaggio, assicurarsi che le categorie siano i primi messaggi del file.</span><span class="sxs-lookup"><span data-stu-id="54dde-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="54dde-113">Per altre informazioni sulla creazione e l'uso di file di messaggio, vedere [file di messaggio](message-files.md).</span><span class="sxs-lookup"><span data-stu-id="54dde-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="54dde-114">Il numero totale di categorie viene archiviato nel valore **CategoryCount** per l'origine evento.</span><span class="sxs-lookup"><span data-stu-id="54dde-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 



