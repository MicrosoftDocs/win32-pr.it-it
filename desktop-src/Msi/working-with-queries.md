---
description: Poiché il programma di installazione utilizza un database relazionale, sono disponibili funzioni che consentono di eseguire query Structured Query Language (SQL) nel database. Nella procedura riportata di seguito viene descritto come utilizzare SQL per eseguire query su un database.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Utilizzo delle query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967728"
---
# <a name="working-with-queries"></a><span data-ttu-id="82ea1-104">Utilizzo delle query</span><span class="sxs-lookup"><span data-stu-id="82ea1-104">Working with Queries</span></span>

<span data-ttu-id="82ea1-105">Poiché il programma di installazione utilizza un database relazionale, sono disponibili funzioni che consentono di eseguire query Structured Query Language (SQL) nel database.</span><span class="sxs-lookup"><span data-stu-id="82ea1-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="82ea1-106">Nella procedura riportata di seguito viene descritto come utilizzare SQL per eseguire query su un database.</span><span class="sxs-lookup"><span data-stu-id="82ea1-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="82ea1-107">**Per eseguire una query su un database con SQL**</span><span class="sxs-lookup"><span data-stu-id="82ea1-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="82ea1-108">Aprire l'oggetto [**View**](view-object.md) , con l'istruzione SQL appropriata, chiamando la funzione [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="82ea1-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="82ea1-109">Un oggetto [**visualizzazione**](view-object.md) è la tabella logica creata applicando una query a un set di tabelle.</span><span class="sxs-lookup"><span data-stu-id="82ea1-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="82ea1-110">Le query SQL devono rispettare la [sintassi SQL](sql-syntax.md) fornita dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="82ea1-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="82ea1-111">Questa istruzione SQL può contenere marcatori di parametro che non vengono specificati fino a quando non viene eseguito l'oggetto **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="82ea1-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="82ea1-112">Eseguire l'oggetto [**View**](view-object.md) chiamando la funzione [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .</span><span class="sxs-lookup"><span data-stu-id="82ea1-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="82ea1-113">Recuperare il record successivo da un oggetto [**visualizzazione**](view-object.md) chiamando la funzione [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .</span><span class="sxs-lookup"><span data-stu-id="82ea1-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="82ea1-114">Modificare l'oggetto [**visualizzazione**](view-object.md) chiamando la funzione [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .</span><span class="sxs-lookup"><span data-stu-id="82ea1-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="82ea1-115">È anche possibile convalidare i dati con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) passando i flag appropriati.</span><span class="sxs-lookup"><span data-stu-id="82ea1-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="82ea1-116">Se **MsiViewModify** restituisce \_ un errore \_ di dati non validi da una richiesta di convalida, i dati sottostanti sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="82ea1-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="82ea1-117">Ottenere informazioni dettagliate sull'errore nell'oggetto [**vista**](view-object.md) chiamando la funzione [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .</span><span class="sxs-lookup"><span data-stu-id="82ea1-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="82ea1-118">Chiudere l'oggetto [**View**](view-object.md) chiamando la funzione [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .</span><span class="sxs-lookup"><span data-stu-id="82ea1-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="82ea1-119">Per ulteriori informazioni, vedere [esempi di query sul database con SQL e script](examples-of-database-queries-using-sql-and-script.md).</span><span class="sxs-lookup"><span data-stu-id="82ea1-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



