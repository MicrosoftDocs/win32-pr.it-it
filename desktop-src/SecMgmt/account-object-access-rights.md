---
description: Il tipo Account Object Access Rights (Diritti di accesso agli oggetti account) dispone dei tipi di accesso seguenti.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Diritti di accesso agli oggetti account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1251eecfd32bc574307cbc4f0f1327e4f96eb7fa7051d1dd638beb59e7ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895108"
---
# <a name="account-object-access-rights"></a>Diritti di accesso agli oggetti account

Il tipo Account Object Access Rights (Diritti di accesso agli oggetti account) dispone dei tipi di accesso seguenti.



| Tipo di accesso                     | Descrizione                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VISUALIZZAZIONE \_ ACCOUNT                   | Questo tipo di accesso è necessario per leggere le informazioni sull'account. Sono inclusi i [*privilegi assegnati*](/windows/desktop/SecGloss/p-gly) all'account, le quote di memoria assegnate ed eventuali tipi di accesso speciali concessi. |
| MODIFICARE \_ I \_ PRIVILEGI DELL'ACCOUNT     | Questo tipo di accesso è necessario per assegnare o rimuovere privilegi da un account.                                                                                                                                                            |
| MODIFICARE \_ \_ LE QUOTE DELL'ACCOUNT         | Questo tipo di accesso è necessario per modificare le quote di sistema assegnate a un account.                                                                                                                                                                      |
| ACCOUNT \_ ADJUST \_ SYSTEM \_ ACCESS | Questo tipo di accesso è necessario per aggiornare i flag di accesso di sistema per l'account.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Maschere di accesso generiche

[**L'oggetto Account**](account-object.md) pubblica i mapping seguenti da tipi di accesso generici a tipi di accesso specifici.

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

Questo oggetto non supporta il tipo di accesso standard SYNCHRONIZE (facoltativo). Sono supportati tutti i tipi di accesso necessari. La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è la seguente.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
