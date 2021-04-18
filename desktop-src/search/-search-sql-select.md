---
description: "Di seguito viene illustrata la sintassi di base dell'istruzione SELECT per una query locale:"
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Istruzione SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306110"
---
# <a name="select-statement"></a><span data-ttu-id="50954-103">Istruzione SELECT</span><span class="sxs-lookup"><span data-stu-id="50954-103">SELECT Statement</span></span>

<span data-ttu-id="50954-104">Di seguito viene illustrata la sintassi di base dell'istruzione SELECT per una query locale:</span><span class="sxs-lookup"><span data-stu-id="50954-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="50954-105">Di seguito viene illustrata la parte della colonna della sintassi dell'istruzione SELECT:</span><span class="sxs-lookup"><span data-stu-id="50954-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="50954-106">Gli identificatori di colonna devono essere colonne di nomi di proprietà valide, separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="50954-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="50954-107">I nomi di colonna validi sono descrizioni di proprietà registrate o sono definiti dallo schema del sistema di proprietà della shell.</span><span class="sxs-lookup"><span data-stu-id="50954-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="50954-108">È possibile selezionare solo le colonne contrassegnate come recuperabili nello schema del sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="50954-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="50954-109">Se si usa il caso misto per identificare le proprietà che non sono proprietà definite dal sistema, è necessario racchiudere l'identificatore di colonna tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="50954-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="50954-110">I nomi di proprietà definiti dal sistema includono tutte le proprietà che iniziano con "System" (ad esempio, System. Contact. FirstName) e non richiedono virgolette.</span><span class="sxs-lookup"><span data-stu-id="50954-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="50954-111">È inoltre possibile racchiudere i nomi delle proprietà definite dal sistema tra virgolette doppie per migliorare la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="50954-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="50954-112">Questa operazione non influisce sulla compatibilità.</span><span class="sxs-lookup"><span data-stu-id="50954-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="50954-113">Quando la query restituisce un documento che non dispone della colonna richiesta, il valore della colonna per il documento è **null**.</span><span class="sxs-lookup"><span data-stu-id="50954-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="50954-114">È necessario specificare almeno un nome di colonna in un'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="50954-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="50954-115">Nella query Structured Query Language (SQL) è possibile utilizzare l'asterisco ( \* ) per specificare che devono essere restituite tutte le colonne di una tabella.</span><span class="sxs-lookup"><span data-stu-id="50954-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="50954-116">Tuttavia, nessun set definito e fisso di proprietà si applica a tutti i documenti.</span><span class="sxs-lookup"><span data-stu-id="50954-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="50954-117">Per questo motivo, l'asterisco SQL non è consentito nell' <columns> identificatore dell'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="50954-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="50954-118">Recupero dei primi n risultati</span><span class="sxs-lookup"><span data-stu-id="50954-118">Getting the Top n Results</span></span>

<span data-ttu-id="50954-119">È possibile specificare un numero massimo di risultati da restituire usando la sintassi TOP:</span><span class="sxs-lookup"><span data-stu-id="50954-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="50954-120">Cast dei tipi di dati delle colonne</span><span class="sxs-lookup"><span data-stu-id="50954-120">Casting Column Data Types</span></span>

<span data-ttu-id="50954-121">In alcuni casi potrebbe essere necessario eseguire il cast dei dati di tipo stringa estratti da documenti come un altro tipo di dati, in modo da poter effettuare un confronto appropriato.</span><span class="sxs-lookup"><span data-stu-id="50954-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="50954-122">Per ulteriori informazioni, fare riferimento a [cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="50954-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="50954-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="50954-123">Examples</span></span>

<span data-ttu-id="50954-124">Negli esempi seguenti vengono restituiti il nome e l'URL dei documenti corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="50954-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="50954-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50954-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="50954-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="50954-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="50954-127">Cast del tipo di dati di una colonna</span><span class="sxs-lookup"><span data-stu-id="50954-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="50954-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="50954-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="50954-129">[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="50954-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



