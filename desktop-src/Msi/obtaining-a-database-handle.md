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
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="8f63f-103">Acquisizione di un handle di database</span><span class="sxs-lookup"><span data-stu-id="8f63f-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="8f63f-104">Prima di utilizzare un database, è necessario innanzitutto ottenere un handle.</span><span class="sxs-lookup"><span data-stu-id="8f63f-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="8f63f-105">**Per accedere alle informazioni relative a un database del programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="8f63f-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="8f63f-106">Ottenere un handle per il database in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f63f-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="8f63f-107">Se è in corso un'installazione, ottenere un handle per il database attivo chiamando la funzione [**funzione MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .</span><span class="sxs-lookup"><span data-stu-id="8f63f-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="8f63f-108">Se non è in corso un'installazione, aprire un database specificato chiamando la funzione [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .</span><span class="sxs-lookup"><span data-stu-id="8f63f-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="8f63f-109">Una volta aperto il database, è possibile chiamare le funzioni per ottenere informazioni sul database o per modificare il database.</span><span class="sxs-lookup"><span data-stu-id="8f63f-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="8f63f-110">Creare un oggetto **visualizzazione** e specificare una query SQL del database aperto chiamando la funzione [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="8f63f-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="8f63f-111">Ottenere un record contenente tutte le chiavi primarie di una tabella specificata nel database aperto chiamando la funzione [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .</span><span class="sxs-lookup"><span data-stu-id="8f63f-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="8f63f-112">Verificare lo stato corrente di un database aperto chiamando la funzione [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) .</span><span class="sxs-lookup"><span data-stu-id="8f63f-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="8f63f-113">Con la funzione **MsiGetDatabaseState** è possibile determinare lo stato di lettura/scrittura per un database o se l'handle è valido.</span><span class="sxs-lookup"><span data-stu-id="8f63f-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



