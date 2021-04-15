---
description: Elenca e illustra i diritti di accesso dell'oggetto dati privato.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Diritti di accesso agli oggetti dati privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484580"
---
# <a name="private-data-object-access-rights"></a>Diritti di accesso agli oggetti dati privati

I tipi di accesso di questo tipo di oggetto sono:



| Tipo di accesso          | Descrizione                                      |
|----------------------|--------------------------------------------------|
| \_valore query \_ Secret | Questo tipo di accesso è necessario per il recupero di un segreto. |
| \_valore imposta \_ segreto   | Questo tipo di accesso è necessario per modificare un segreto.   |



 

## <a name="generic-access-masks"></a>Maschere di accesso generico

Questo tipo di oggetto ha i mapping di accesso generici seguenti:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Tipi di accesso standard:

Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE. Sono supportati tutti i tipi di accesso necessari. La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



