---
description: Il tipo di dati CAB deve essere utilizzato nella colonna CAB della tabella dei supporti.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881066"
---
# <a name="cabinet"></a>CAB

Il tipo di dati CAB deve essere utilizzato nella colonna CAB della [tabella dei supporti](media-table.md).

Se il nome del cabinet è preceduto dal simbolo di cancelletto, il file CAB viene archiviato come flusso di dati all'interno del pacchetto. La stringa di caratteri che segue \# è un [identificatore](identifier.md) per questo flusso di dati. Si noti che se l'archivio è archiviato come flusso di dati, il nome di un file CAB fa distinzione tra maiuscole e minuscole.

Se il nome del cabinet non è preceduto dal simbolo di cancelletto \# , il file CAB viene archiviato in un file separato che si trova nella radice dell'albero di origine specificato dalla [tabella di directory](directory-table.md). Il file CAB deve usare la sintassi del nome file breve costituito da un nome di otto caratteri, un punto e un'estensione di tre caratteri. Il tipo di dati CAB non può utilizzare la \| sintassi Short LongName per i nomi di file. Se il file CAB viene archiviato come file separato, il nome del file CAB non distingue tra maiuscole e minuscole.

Per conservare spazio su disco, il programma di installazione rimuove tutti i cabinet incorporati nel file con estensione msi prima di memorizzare nella cache il pacchetto di installazione nel computer dell'utente.

Vedere [inclusione di un file CAB in un'installazione](including-a-cabinet-file-in-an-installation.md).

 

 



