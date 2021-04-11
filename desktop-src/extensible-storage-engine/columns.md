---
description: 'Altre informazioni su: colonne'
title: Colonne
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130207"
---
# <a name="columns"></a><span data-ttu-id="63eda-103">Colonne</span><span class="sxs-lookup"><span data-stu-id="63eda-103">Columns</span></span>


<span data-ttu-id="63eda-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="63eda-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="63eda-105">Colonne</span><span class="sxs-lookup"><span data-stu-id="63eda-105">Columns</span></span>

<span data-ttu-id="63eda-106">È possibile creare una tabella con un set iniziale di colonne chiamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o senza un set iniziale di colonne chiamando [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="63eda-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="63eda-107">Le tabelle in ESE possono contenere fino a 127 colonne a lunghezza fissa, 128 colonne a lunghezza variabile e 64.993 colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="63eda-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="63eda-108">Le colonne vengono identificate in base al nome e all'ID e possono essere aggiunte dinamicamente alla tabella con [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="63eda-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="63eda-109">Le colonne vengono create con un tipo di dati specifico e un set facoltativo di attributi, ad esempio se la colonna è a lunghezza fissa o se può essere NULL o meno.</span><span class="sxs-lookup"><span data-stu-id="63eda-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="63eda-110">Il tipo di una colonna determina i dati che possono essere archiviati nella colonna e molte delle proprietà della colonna, incluso l'ordine per l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="63eda-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="63eda-111">ESE supporta un'ampia gamma di tipi di colonna, con dimensioni comprese tra 1 bit e 2 GB (2146483647 caratteri ASCII o 1073741823 caratteri Unicode).</span><span class="sxs-lookup"><span data-stu-id="63eda-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="63eda-112">Per un elenco completo dei tipi di dati delle colonne supportati da ESE, vedere l'argomento [JET_COLTYP](./jet-coltyp.md) .</span><span class="sxs-lookup"><span data-stu-id="63eda-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="63eda-113">Negli argomenti seguenti vengono illustrati alcuni tipi di colonne supportati da ESE:</span><span class="sxs-lookup"><span data-stu-id="63eda-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="63eda-114">Colonne con tag, fisse e variabili</span><span class="sxs-lookup"><span data-stu-id="63eda-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="63eda-115">Colonne versione, incremento automatico e escrow</span><span class="sxs-lookup"><span data-stu-id="63eda-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="63eda-116">Colonne con valore Long</span><span class="sxs-lookup"><span data-stu-id="63eda-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="63eda-117">Colonne di tipo sparse multivalore</span><span class="sxs-lookup"><span data-stu-id="63eda-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="63eda-118">Colonne definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="63eda-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="63eda-119">Utilizzo di colonne in una tabella</span><span class="sxs-lookup"><span data-stu-id="63eda-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
