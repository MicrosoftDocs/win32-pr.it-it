---
description: Se l'origine dati è un file di log, è possibile specificare un intervallo di tempo per la query.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Impostazione di un intervallo di tempo per una query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312086"
---
# <a name="setting-a-time-range-for-a-query"></a>Impostazione di un intervallo di tempo per una query

Se l'origine dati è un file di log, è possibile specificare un intervallo di tempo per la query. La query recupera i dati del contatore dal file di log raccolto durante l'intervallo di tempo specificato. Per impostare l'intervallo di tempo, chiamare la funzione [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) . **PdhSetQueryTimeRange** non viene utilizzato per eseguire query sui dati sulle prestazioni da origini dati in tempo reale.

Per creare un valore di ora, attenersi alla procedura riportata di seguito.

1.  Allocare una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inizializzare i campi con il valore di ora desiderato.
2.  Chiamare [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) per convertire il valore dell'ora della struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in un'ora di struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
3.  Eseguire il cast della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) come variabile LONGLONG, tenendo presente le convenzioni di riempimento dei membri della struttura della piattaforma e del compilatore.
4.  Copiare il valore LONGLONG nel campo appropriato nella struttura [**PDH \_ time \_ info**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .

Per recuperare l'intervallo di tempo di tutti i dati sulle prestazioni contenuti in un file di log, chiamare la funzione [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .

 

 
