---
description: Gli identificatori specificano i nomi delle colonne (talvolta denominate proprietà), i cataloghi e gli alias.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128539"
---
# <a name="identifiers"></a><span data-ttu-id="6d837-103">Identificatori</span><span class="sxs-lookup"><span data-stu-id="6d837-103">Identifiers</span></span>

<span data-ttu-id="6d837-104">Gli identificatori specificano i nomi delle colonne (talvolta denominate proprietà), i cataloghi e gli alias.</span><span class="sxs-lookup"><span data-stu-id="6d837-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="6d837-105">Ad esempio, System. ItemName e System. DateCreated sono gli identificatori di due colonne di proprietà definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6d837-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="6d837-106">I valori letterali, al contrario, specificano valori stringa e numerici.</span><span class="sxs-lookup"><span data-stu-id="6d837-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="6d837-107">È possibile creare identificatori costituiti da un massimo di 128 caratteri e in uno dei due tipi distinti in base ai caratteri utilizzati nel nome dell'identificatore:</span><span class="sxs-lookup"><span data-stu-id="6d837-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="6d837-108">Gli **identificatori regolari** contengono solo i caratteri a-z, a-z, 0-9, il carattere di sottolineatura ( \_ ) e il punto (.) e iniziano con una lettera.</span><span class="sxs-lookup"><span data-stu-id="6d837-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="6d837-109">Non è necessario racchiudere gli identificatori regolari racchiusi tra virgolette doppie ("").</span><span class="sxs-lookup"><span data-stu-id="6d837-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="6d837-110">Gli **identificatori delimitati** possono contenere qualsiasi carattere Unicode valido e devono essere racchiusi tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="6d837-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="6d837-111">Nelle clausole FREETEXT e CONTAINs è possibile utilizzare l'asterisco ( \* ) come identificatore di colonna speciale quando si desidera specificare che Windows Search includa tutte le proprietà indicizzate nella query.</span><span class="sxs-lookup"><span data-stu-id="6d837-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="6d837-112">Sebbene non sia un identificatore regolare, non richiede virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="6d837-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



