---
description: La routine di callback della coda predefinita può essere specificata per gestire le notifiche inviate da SetupCommitFileQueue oppure può essere chiamata da una routine di callback personalizzata che si basa sulla funzionalità della routine di callback della coda predefinita.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Uso della routine di callback della coda predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311920"
---
# <a name="using-the-default-queue-callback-routine"></a>Uso della routine di callback della coda predefinita

La routine di callback della coda predefinita può essere specificata per gestire le notifiche inviate da [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)oppure può essere chiamata da una routine di callback personalizzata che si basa sulla funzionalità della routine di callback della coda predefinita.

Nelle sezioni seguenti viene illustrato come inizializzare e terminare il contesto utilizzato da una routine di callback della coda predefinita. Le sezioni descrivono anche come usare la routine di callback della coda predefinita con [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) o una routine di callback personalizzata.

-   [Inizializzazione e terminazione del contesto di callback](initializing-and-terminating-the-callback-context.md)
-   [Chiamata della routine di callback della coda predefinita](calling-the-default-queue-callback-routine.md)

 

 



