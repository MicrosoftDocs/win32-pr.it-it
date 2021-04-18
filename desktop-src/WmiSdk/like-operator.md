---
description: L'operatore LIKE determina se una stringa di caratteri corrisponde a un criterio specificato.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operatore LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310346"
---
# <a name="like-operator"></a><span data-ttu-id="71310-103">Operatore LIKE</span><span class="sxs-lookup"><span data-stu-id="71310-103">LIKE Operator</span></span>

<span data-ttu-id="71310-104">L'operatore LIKE determina se una stringa di caratteri corrisponde a un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="71310-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="71310-105">Il modello specificato può contenere esattamente i caratteri per cui trovare una corrispondenza oppure può contenere caratteri meta.</span><span class="sxs-lookup"><span data-stu-id="71310-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="71310-106">In effetti, l'operatore LIKE corrisponde a sottostringhe che usano i caratteri jolly nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="71310-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="71310-107">Carattere</span><span class="sxs-lookup"><span data-stu-id="71310-107">Character</span></span>       | <span data-ttu-id="71310-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71310-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71310-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="71310-109">\[ \]</span></span>           | <span data-ttu-id="71310-110">Qualsiasi carattere compreso nell'intervallo specificato ( \[ a-f \] ) o set ( \[ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="71310-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="71310-111">Qualsiasi carattere non compreso nell'intervallo ( \[ ^ a-f \] ) o set ( \[ ^ abcdef \] .)</span><span class="sxs-lookup"><span data-stu-id="71310-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="71310-112">Qualsiasi stringa di 0 (zero) o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="71310-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="71310-113">Nell'esempio seguente vengono individuate tutte le istanze in cui "Win" si trova in un punto qualsiasi nel nome della classe: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="71310-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="71310-114">\_ sottolineatura</span><span class="sxs-lookup"><span data-stu-id="71310-114">\_ (underscore)</span></span> | <span data-ttu-id="71310-115">Qualsiasi carattere.</span><span class="sxs-lookup"><span data-stu-id="71310-115">Any one character.</span></span> <span data-ttu-id="71310-116">Qualsiasi carattere di sottolineatura letterale usato nella stringa di query deve essere preceduto da un carattere di escape inserendolo all'interno di parentesi quadre \[ \] .</span><span class="sxs-lookup"><span data-stu-id="71310-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="71310-117">Il codice di Power Shell seguente, ad esempio, recupera tutte le istanze della classe **Win32 \_ OperatingSystem** la cui proprietà **Name** inizia con **FirstName**:</span><span class="sxs-lookup"><span data-stu-id="71310-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="71310-118">Poiché il carattere di sottolineatura è un carattere meta, se la destinazione della query ha un carattere di sottolineatura, i \[ \] caratteri di escape "" devono racchiuderlo.</span><span class="sxs-lookup"><span data-stu-id="71310-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="71310-119">Ad esempio, è possibile eseguire una query per tutte le classi con un doppio carattere di sottolineatura nel nome.</span><span class="sxs-lookup"><span data-stu-id="71310-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="71310-120">Per individuare tutte le classi con un doppio carattere di sottolineatura nel nome, è necessario eseguire l'escape di entrambi i caratteri di sottolineatura con \[ \] (parentesi quadre), ad esempio:</span><span class="sxs-lookup"><span data-stu-id="71310-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="71310-121">È possibile negare un'istruzione LIKE usando NOT; a tale scopo, assicurarsi di collocare l'oggetto non direttamente davanti al nome del campo.</span><span class="sxs-lookup"><span data-stu-id="71310-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="71310-122">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="71310-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="71310-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71310-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71310-124">Operatori WQL</span><span class="sxs-lookup"><span data-stu-id="71310-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



