---
description: Un'applicazione visualizzatore eventi usa la funzione OpenEventLog per aprire il registro eventi per un'origine evento.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lettura dal registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d0756ba7d9609bca285ce33d69738984badf7effff8867fc5c3e1943b09145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151537"
---
# <a name="reading-from-the-event-log"></a>Lettura dal registro eventi

Un'applicazione visualizzatore eventi usa [**la funzione OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) per aprire il registro eventi per un'origine evento. Il visualizzatore eventi può quindi usare la [**funzione ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) per leggere i record degli eventi dal log. **ReadEventLog restituisce** un buffer contenente una [**struttura EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e informazioni aggiuntive che descrivono un evento registrato. La figura seguente illustra questo processo.

![lettura dal registro eventi](images/readlog.png)

Per un esempio di codice, vedere [Querying for Event Information](querying-for-event-source-messages.md).

 

 



