---
description: Prima di utilizzare un database, è necessario innanzitutto ottenere un handle.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Acquisizione di un handle di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130439"
---
# <a name="obtaining-a-database-handle"></a>Acquisizione di un handle di database

Prima di utilizzare un database, è necessario innanzitutto ottenere un handle.

**Per accedere alle informazioni relative a un database del programma di installazione**

1.  Ottenere un handle per il database in uno dei due modi seguenti:
    -   Se è in corso un'installazione, ottenere un handle per il database attivo chiamando la funzione [**funzione MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .
    -   Se non è in corso un'installazione, aprire un database specificato chiamando la funzione [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .
2.  Una volta aperto il database, è possibile chiamare le funzioni per ottenere informazioni sul database o per modificare il database.
    -   Creare un oggetto **visualizzazione** e specificare una query SQL del database aperto chiamando la funzione [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .
    -   Ottenere un record contenente tutte le chiavi primarie di una tabella specificata nel database aperto chiamando la funzione [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .
    -   Verificare lo stato corrente di un database aperto chiamando la funzione [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) . Con la funzione **MsiGetDatabaseState** è possibile determinare lo stato di lettura/scrittura per un database o se l'handle è valido.

 

 



