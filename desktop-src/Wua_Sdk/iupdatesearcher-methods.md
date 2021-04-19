---
description: L'interfaccia IUpdateSearcher definisce i metodi seguenti.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Metodi IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307601"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="36aa5-103">Metodi IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="36aa5-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="36aa5-104">L'interfaccia [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) definisce i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="36aa5-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="36aa5-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="36aa5-105">Method</span></span>                                                              | <span data-ttu-id="36aa5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36aa5-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36aa5-107">**BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="36aa5-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="36aa5-108">Inizia l'esecuzione di una ricerca asincrona degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="36aa5-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="36aa5-109">La ricerca usa le opzioni di ricerca attualmente configurate.</span><span class="sxs-lookup"><span data-stu-id="36aa5-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="36aa5-110">**EndSearch**</span><span class="sxs-lookup"><span data-stu-id="36aa5-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="36aa5-111">Completa una ricerca asincrona di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="36aa5-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="36aa5-112">**EscapeString**</span><span class="sxs-lookup"><span data-stu-id="36aa5-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="36aa5-113">Converte una stringa in una stringa che può essere utilizzata come valore letterale in una stringa di criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="36aa5-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="36aa5-114">**GetTotalHistoryCount**</span><span class="sxs-lookup"><span data-stu-id="36aa5-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="36aa5-115">Restituisce il numero di eventi di aggiornamento nel computer.</span><span class="sxs-lookup"><span data-stu-id="36aa5-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="36aa5-116">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="36aa5-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="36aa5-117">Esegue una query in modo sincrono sul computer per la cronologia degli eventi di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="36aa5-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="36aa5-118">**Cerca**</span><span class="sxs-lookup"><span data-stu-id="36aa5-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="36aa5-119">Esegue una ricerca sincrona degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="36aa5-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="36aa5-120">La ricerca usa le opzioni di ricerca attualmente configurate.</span><span class="sxs-lookup"><span data-stu-id="36aa5-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 



