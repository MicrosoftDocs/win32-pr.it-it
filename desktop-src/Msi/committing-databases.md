---
description: Le modifiche apportate al database di installazione non vengono scritte nel database fino a quando non si chiama MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Commit di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1ab5f4da5b82fb3b6b2ac7d2371bd8046ab87a23d2ef43b6473f7e36a4771a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145350"
---
# <a name="committing-databases"></a>Commit di database

Le modifiche apportate al database di installazione non vengono scritte nel database fino a quando non si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Per assicurarsi che le modifiche apportate in un database siano finalizzate**

1.  Verificare se verrà scritta una tabella quando si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) chiamando [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Chiamare la [**funzione MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) per finalizzare le modifiche al database.

Le modifiche apportate in un database vengono accumulate e non vengono riflesse nel database effettivo fino a quando non si chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Non viene eseguito il commit di colonne o righe temporanee nel database. Quando un database viene chiuso, viene eseguito automaticamente il rollback di tutte le modifiche apportate dopo l'ultimo **MsiDatabaseCommit.**

 

 



