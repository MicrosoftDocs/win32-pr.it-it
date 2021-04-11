---
description: Un'applicazione Visualizzatore eventi utilizza la funzione OpenEventLog per aprire il registro eventi per un'origine evento.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lettura dal registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049854"
---
# <a name="reading-from-the-event-log"></a>Lettura dal registro eventi

Un'applicazione Visualizzatore eventi utilizza la funzione [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) per aprire il registro eventi per un'origine evento. Il Visualizzatore eventi può quindi utilizzare la funzione [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) per leggere i record di eventi dal log. **ReadEventLog** restituisce un buffer contenente una struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e informazioni aggiuntive che descrivono un evento registrato. La figura seguente illustra questo processo.

![lettura dal registro eventi](images/readlog.png)

Per un esempio di codice, vedere [esecuzione di query per informazioni sull'evento](querying-for-event-source-messages.md).

 

 



