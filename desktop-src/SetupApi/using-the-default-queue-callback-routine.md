---
description: La routine di callback della coda predefinita può essere specificata per gestire le notifiche inviate da SetupCommitFileQueue oppure può essere chiamata da una routine di callback personalizzata che si basa sulla funzionalità della routine di callback della coda predefinita.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Uso della routine di callback della coda predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32515956d790267e1506ecee2afe50cc1fbd468562084b5b44aa8e29a32c8b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963970"
---
# <a name="using-the-default-queue-callback-routine"></a>Uso della routine di callback della coda predefinita

La routine di callback della coda predefinita può essere specificata per gestire le notifiche inviate da [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)oppure può essere chiamata da una routine di callback personalizzata che si basa sulla funzionalità della routine di callback della coda predefinita.

Nelle sezioni seguenti viene illustrato come inizializzare e terminare il contesto utilizzato da una routine di callback della coda predefinita. Le sezioni descrivono anche come usare la routine di callback della coda predefinita [**con SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) o una routine di callback personalizzata.

-   [Inizializzazione e terminazione del contesto di callback](initializing-and-terminating-the-callback-context.md)
-   [Chiamata della routine di callback predefinita della coda](calling-the-default-queue-callback-routine.md)

 

 



