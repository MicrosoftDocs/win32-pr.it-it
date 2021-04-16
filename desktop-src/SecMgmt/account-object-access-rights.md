---
description: Il tipo di diritti di accesso agli oggetti account ha i seguenti tipi di accesso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Diritti di accesso agli oggetti account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529647"
---
# <a name="account-object-access-rights"></a>Diritti di accesso agli oggetti account

Il tipo di diritti di accesso agli oggetti account ha i seguenti tipi di accesso.



| Tipo di accesso                     | Descrizione                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_visualizzazione account                   | Questo tipo di accesso è necessario per leggere le informazioni sull'account. Sono inclusi i [*privilegi*](/windows/desktop/SecGloss/p-gly) assegnati all'account, le quote di memoria assegnate e tutti i tipi di accesso speciali concessi. |
| privilegi per la modifica dell'ACCOUNT \_ \_     | Questo tipo di accesso è necessario per assegnare o rimuovere privilegi da un account.                                                                                                                                                            |
| \_quote di regolazione dell'account \_         | Questo tipo di accesso è necessario per modificare le quote di sistema assegnate a un account.                                                                                                                                                                      |
| ACCOUNT \_ per \_ regolare \_ l'accesso al sistema | Questo tipo di accesso è necessario per aggiornare i flag di accesso al sistema per l'account.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Maschere di accesso generico

L'oggetto [**account**](account-object.md) pubblica i mapping seguenti dai tipi di accesso generici ai tipi di accesso specifici.

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Tipi di accesso standard

Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE. Sono supportati tutti i tipi di accesso necessari. Di seguito è riportata la maschera di tutti i tipi di accesso supportati per questo tipo di oggetto.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
