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
# <a name="committing-databases"></a>Commit dei database

Le modifiche apportate al database di installazione non vengono scritte nel database fino a quando non si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Per assicurarsi che le modifiche apportate in un database vengano finalizzate**

1.  Verificare se una tabella verrà scritta quando si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) chiamando [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Chiamare la funzione [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) per finalizzare le modifiche al database.

Le modifiche apportate in un database vengono accumulate e non vengono riflesse nel database effettivo fino a quando non si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Al database non viene eseguito il commit di righe o colonne temporanee. Quando un database viene chiuso, viene eseguito automaticamente il rollback di tutte le modifiche apportate dopo l'ultimo **MsiDatabaseCommit** .

 

 



