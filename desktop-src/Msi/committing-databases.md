---
description: Le modifiche apportate al database di installazione non vengono scritte nel database fino a quando non si chiama MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Commit dei database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883369"
---
# <a name="committing-databases"></a><span data-ttu-id="eca1d-103">Commit dei database</span><span class="sxs-lookup"><span data-stu-id="eca1d-103">Committing Databases</span></span>

<span data-ttu-id="eca1d-104">Le modifiche apportate al database di installazione non vengono scritte nel database fino a quando non si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="eca1d-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="eca1d-105">**Per assicurarsi che le modifiche apportate in un database vengano finalizzate**</span><span class="sxs-lookup"><span data-stu-id="eca1d-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="eca1d-106">Verificare se una tabella verrà scritta quando si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) chiamando [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span><span class="sxs-lookup"><span data-stu-id="eca1d-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="eca1d-107">Chiamare la funzione [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) per finalizzare le modifiche al database.</span><span class="sxs-lookup"><span data-stu-id="eca1d-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="eca1d-108">Le modifiche apportate in un database vengono accumulate e non vengono riflesse nel database effettivo fino a quando non si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="eca1d-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="eca1d-109">Al database non viene eseguito il commit di righe o colonne temporanee.</span><span class="sxs-lookup"><span data-stu-id="eca1d-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="eca1d-110">Quando un database viene chiuso, viene eseguito automaticamente il rollback di tutte le modifiche apportate dopo l'ultimo **MsiDatabaseCommit** .</span><span class="sxs-lookup"><span data-stu-id="eca1d-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



