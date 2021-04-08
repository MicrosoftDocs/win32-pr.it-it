---
description: Le informazioni relative a ogni evento vengono archiviate nel registro eventi in un record del registro eventi. Il record del registro eventi include informazioni su tempo, tipo e categoria. Per ulteriori informazioni, vedere la struttura EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Record del registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880893"
---
# <a name="event-log-records"></a>Record del registro eventi

Le informazioni relative a ogni evento vengono archiviate nel registro eventi in un *record del registro eventi*. Il record del registro eventi include informazioni su tempo, tipo e categoria. Per ulteriori informazioni, vedere la struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .

Il membro **RecordNumber** di [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contiene il numero di record per il record del log eventi. Il primo record scritto in un log eventi è il numero di record 1 e gli altri record sono numerati in sequenza. Se il numero di record raggiunge ULONG \_ Max, il numero di record successivo sarà 0, non 1, ma si userà zero per cercare il record.

Se il valore del registro di sistema [conservazione](eventlog-key.md) è impostato su zero, i record degli eventi vengono sovrascritti quando viene raggiunta la dimensione massima del log. Il record meno recente in un log eventi, quindi, non può essere un record numero 1. Per identificare il record meno recente nel log, chiamare la funzione [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) . È quindi possibile chiamare la funzione [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) e aggiungere il valore restituito al numero di record meno recente per determinare il record più recente.

È possibile leggere singoli record dal registro eventi usando la funzione [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) . Per ulteriori informazioni, vedere [esecuzione di query per informazioni sull'evento](querying-for-event-source-messages.md).

 

 



