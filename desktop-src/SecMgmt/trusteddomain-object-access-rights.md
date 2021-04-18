---
description: Elenca e illustra i diritti di accesso dell'oggetto TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Diritti di accesso agli oggetti TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306414"
---
# <a name="trusteddomain-object-access-rights"></a>Diritti di accesso agli oggetti TrustedDomain

Il tipo di oggetto [**trustedDomain**](trusteddomain-object.md) presenta i tipi di accesso seguenti:



| Tipo di accesso                  | Descrizione                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| \_nome di \_ dominio di query attendibile \_ | Questo tipo di accesso è necessario per eseguire una query sul nome del dominio attendibile.              |
| \_Controller Set attendibili \_    | Questo tipo di accesso è necessario per impostare l'elenco dei controller del dominio trusted. |
| QUERY ATTENDIBILe \_ \_ POSIX        | Questo tipo di accesso è necessario per recuperare l'offset dell'ID POSIX di un dominio trusted.  |
| SET ATTENDIBILe \_ \_ POSIX          | Questo tipo di accesso è necessario per impostare l'offset dell'ID POSIX di un dominio trusted.       |



 

## <a name="generic-access-masks"></a>Maschere di accesso generico

Questo tipo di oggetto ha i mapping di accesso generici seguenti:

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Tipi di accesso standard

Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE. Sono supportati tutti i tipi di accesso necessari. La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



