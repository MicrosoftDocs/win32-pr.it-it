---
description: La \_ tabella Tables è una tabella di sistema di sola lettura in cui sono elencate tutte le tabelle del database. Eseguire una query su questa tabella per verificare se esiste una tabella.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Tabella _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881189"
---
# <a name="_tables-table"></a><span data-ttu-id="502d4-104">\_Tabella tabelle</span><span class="sxs-lookup"><span data-stu-id="502d4-104">\_Tables Table</span></span>

<span data-ttu-id="502d4-105">La \_ tabella Tables è una tabella di sistema di sola lettura in cui sono elencate tutte le tabelle del database.</span><span class="sxs-lookup"><span data-stu-id="502d4-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="502d4-106">Eseguire una query su questa tabella per verificare se esiste una tabella.</span><span class="sxs-lookup"><span data-stu-id="502d4-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="502d4-107">La \_ tabella tables contiene la seguente colonna.</span><span class="sxs-lookup"><span data-stu-id="502d4-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="502d4-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="502d4-108">Column</span></span> | <span data-ttu-id="502d4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="502d4-109">Type</span></span>             | <span data-ttu-id="502d4-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="502d4-110">Key</span></span> | <span data-ttu-id="502d4-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="502d4-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="502d4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="502d4-112">Name</span></span>   | [<span data-ttu-id="502d4-113">Text</span><span class="sxs-lookup"><span data-stu-id="502d4-113">Text</span></span>](text.md) | <span data-ttu-id="502d4-114">S</span><span class="sxs-lookup"><span data-stu-id="502d4-114">Y</span></span>   | <span data-ttu-id="502d4-115">N</span><span class="sxs-lookup"><span data-stu-id="502d4-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="502d4-116">Colonna</span><span class="sxs-lookup"><span data-stu-id="502d4-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="502d4-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="502d4-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="502d4-118">Nome di una delle tabelle.</span><span class="sxs-lookup"><span data-stu-id="502d4-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="502d4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="502d4-119">Remarks</span></span>

<span data-ttu-id="502d4-120">Poiché la \_ tabella Tables è una tabella di sistema che non può essere modificata tramite query SQL, non è possibile ottenere le chiavi primarie con la funzione [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**Proprietà PrimaryKeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="502d4-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



