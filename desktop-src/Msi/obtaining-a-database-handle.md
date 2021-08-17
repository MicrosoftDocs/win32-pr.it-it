---
description: Prima di utilizzare un database, è necessario ottenere un handle per il database.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Recupero di un handle di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a325c7c69bed4141de8f553a344b20b5f3c61bfe28a1594105c0a853b7075744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145564"
---
# <a name="obtaining-a-database-handle"></a>Recupero di un handle di database

Prima di utilizzare un database, è necessario ottenere un handle per il database.

**Per accedere alle informazioni su un database del programma di installazione**

1.  Ottenere un handle per il database in uno dei due modi seguenti:
    -   Se è in corso un'installazione, ottenere un handle per il database attivo chiamando la [**funzione MsiGetActiveDatabase.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)
    -   Se non è in corso un'installazione, aprire un database specificato chiamando la [**funzione MsiOpenDatabase.**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
2.  Dopo aver aperto il database, è possibile chiamare le funzioni per ottenere informazioni sul database o per modificare il database.
    -   Creare un **oggetto View** e specificare una SQL query del database aperto chiamando la [**funzione MsiDatabaseOpenView.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)
    -   Ottenere un record che contiene tutte le chiavi primarie di una tabella specificata nel database aperto chiamando la [**funzione MsiDatabaseGetPrimaryKeys.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)
    -   Controllare lo stato corrente di un database aperto chiamando la [**funzione MsiGetDatabaseState.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) Con la **funzione MsiGetDatabaseState** è possibile determinare lo stato di lettura/scrittura per un database o se l'handle è valido.

 

 



