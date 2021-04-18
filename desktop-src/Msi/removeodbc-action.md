---
description: L'azione RemoveODBC rimuove le origini dati, i traduttori e i driver elencati per la rimozione durante l'installazione.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Azione RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312319"
---
# <a name="removeodbc-action"></a><span data-ttu-id="94c60-103">Azione RemoveODBC</span><span class="sxs-lookup"><span data-stu-id="94c60-103">RemoveODBC Action</span></span>

<span data-ttu-id="94c60-104">L'azione RemoveODBC rimuove le origini dati, i traduttori e i driver elencati per la rimozione durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="94c60-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="94c60-105">Questa azione esegue una query sulla tabella [ODBCDataSource](odbcdatasource-table.md), sulla [tabella ODBCTranslator](odbctranslator-table.md)e sulla [tabella ODBCDriver](odbcdriver-table.md) per ogni origine dati, convertitore o driver pianificato per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="94c60-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="94c60-106">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="94c60-106">Sequence Restrictions</span></span>

<span data-ttu-id="94c60-107">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="94c60-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="94c60-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="94c60-108">ActionData Messages</span></span>

<span data-ttu-id="94c60-109">Per ogni driver installato.</span><span class="sxs-lookup"><span data-stu-id="94c60-109">For each driver installed.</span></span>



| <span data-ttu-id="94c60-110">Campo</span><span class="sxs-lookup"><span data-stu-id="94c60-110">Field</span></span> | <span data-ttu-id="94c60-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="94c60-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="94c60-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="94c60-112">\[1\]</span></span> | <span data-ttu-id="94c60-113">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="94c60-113">Driver description.</span></span> <span data-ttu-id="94c60-114">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="94c60-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="94c60-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="94c60-115">\[2\]</span></span> | <span data-ttu-id="94c60-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="94c60-116">ComponentId</span></span>                              |



 

<span data-ttu-id="94c60-117">Per ogni traduttore installato.</span><span class="sxs-lookup"><span data-stu-id="94c60-117">For each translator installed.</span></span>



| <span data-ttu-id="94c60-118">Campo</span><span class="sxs-lookup"><span data-stu-id="94c60-118">Field</span></span> | <span data-ttu-id="94c60-119">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="94c60-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="94c60-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="94c60-120">\[1\]</span></span> | <span data-ttu-id="94c60-121">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="94c60-121">Driver description.</span></span> <span data-ttu-id="94c60-122">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="94c60-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="94c60-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="94c60-123">\[2\]</span></span> | <span data-ttu-id="94c60-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="94c60-124">ComponentId</span></span>                              |



 

<span data-ttu-id="94c60-125">Per ogni origine dati installata.</span><span class="sxs-lookup"><span data-stu-id="94c60-125">For each data source installed.</span></span>



| <span data-ttu-id="94c60-126">Campo</span><span class="sxs-lookup"><span data-stu-id="94c60-126">Field</span></span> | <span data-ttu-id="94c60-127">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="94c60-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="94c60-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="94c60-128">\[1\]</span></span> | <span data-ttu-id="94c60-129">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="94c60-129">Driver description.</span></span> <span data-ttu-id="94c60-130">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="94c60-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="94c60-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="94c60-131">\[2\]</span></span> | <span data-ttu-id="94c60-132">ComponentId</span><span class="sxs-lookup"><span data-stu-id="94c60-132">ComponentId</span></span>                                             |
| <span data-ttu-id="94c60-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="94c60-133">\[3\]</span></span> | <span data-ttu-id="94c60-134">Registrazione: SQL \_ Remove \_ DSN o SQL \_ Remove \_ sys \_ DSN</span><span class="sxs-lookup"><span data-stu-id="94c60-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="94c60-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="94c60-135">Remarks</span></span>

<span data-ttu-id="94c60-136">Se il conteggio di utilizzo di ODBC e il conteggio di utilizzo file diventano zero, il file verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="94c60-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="94c60-137">La registrazione dipende dai conteggi di utilizzo di ODBC e la rimozione dei file è basata sui conteggi dei riferimenti chiave delle DLL condivise.</span><span class="sxs-lookup"><span data-stu-id="94c60-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



