---
description: COMREPL esegue il proprio lavoro in tre fasi.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fasi di replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d1924b85e2681854fe8de604fea1fe59a022fa97843051457677905048dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990421"
---
# <a name="replication-phases"></a>Fasi di replica

COMREPL esegue il proprio lavoro in tre fasi. Il processo di replica è suddiviso in fasi distinte per i due motivi seguenti:

-   Per separare il lavoro svolto per preparare l'origine dal lavoro eseguito in ogni destinazione
-   Per ritardare la modifica della destinazione fino a quando non sono stati acquisiti tutti i dati dall'origine

Le fasi di replica sono le seguenti.



| Fase         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase preparatoria | Esporta tutte le applicazioni installate localmente nel computer di origine. Questa fase non influisce sulla configurazione delle destinazioni.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fase di copia    | Copia i dati in un computer di destinazione. Tutte le applicazioni esportate nell'origine vengono copiate nella destinazione. Si tratta di un'operazione di copia di file. Vedere [Gestione file.](file-management.md) Questo passaggio acquisisce anche alcuni dati dal computer di origine non incapsulati all'interno dei file dell'applicazione esportati, ad esempio le identità dell'applicazione. Questi dati vengono mantenuti in memoria all'interno di COMREPL. Questa fase non influisce sulla configurazione dei computer di destinazione.                                                                               |
| Fase di installazione | Installa il catalogo di origine in un computer di destinazione. Quando questo passaggio viene avviato, tutti i dati necessari per riconfigurare la destinazione si trova all'interno dei file dell'applicazione nel file system della destinazione o vengono mantenuti come dati dell'istanza all'interno di COMREPL. Questa fase eliminerà tutte le applicazioni installate nella destinazione (ad eccezione delle applicazioni descritte in [Elementi](what-gets-replicated.md)replicati) prima di installare le applicazioni copiate dall'origine. COMREPL viene installato contemporaneamente in più destinazioni usando un thread di installazione per ogni destinazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> <dt>

[Elementi replicati](what-gets-replicated.md)
</dt> </dl>

 

 



