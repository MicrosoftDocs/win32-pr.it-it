---
description: COMREPL funziona in tre fasi.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fasi di replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305210"
---
# <a name="replication-phases"></a>Fasi di replica

COMREPL funziona in tre fasi. Il processo di replica è suddiviso in fasi distinte per i due motivi seguenti:

-   Per separare il lavoro svolto per preparare l'origine dal lavoro eseguito in ogni destinazione
-   Per ritardare la modifica della destinazione fino a quando tutti i dati non sono stati acquisiti dall'origine

Di seguito sono riportate le fasi di replica.



| Fase         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase preparatoria | Esporta tutte le applicazioni installate localmente nel computer di origine. Questa fase non tocca la configurazione di alcuna destinazione.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fase di copia    | Copia i dati in un computer di destinazione. Tutte le applicazioni esportate nell'origine vengono copiate nella destinazione. Si tratta di un'operazione di copia file. Vedere [Gestione file](file-management.md). Questo passaggio acquisisce anche alcuni dati dal computer di origine che non è incapsulato all'interno dei file dell'applicazione esportati, ad esempio le identità dell'applicazione. Questi dati vengono conservati in memoria all'interno di COMREPL. Questa fase non tocca la configurazione dei computer di destinazione.                                                                               |
| Fase di installazione | Installa il catalogo di origine in un computer di destinazione. Quando questo passaggio viene avviato, tutti i dati necessari per riconfigurare la destinazione si trovano all'interno dei file dell'applicazione nella file system della destinazione o vengono mantenuti come dati di istanza all'interno di COMREPL. Questa fase eliminerà tutte le applicazioni installate nella destinazione (ad eccezione delle applicazioni descritte in [ciò che viene replicato](what-gets-replicated.md)) prima di installare le applicazioni copiate dall'origine. COMREPL viene installato su più destinazioni contemporaneamente usando un thread di installazione per destinazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> <dt>

[Cosa viene replicato](what-gets-replicated.md)
</dt> </dl>

 

 



