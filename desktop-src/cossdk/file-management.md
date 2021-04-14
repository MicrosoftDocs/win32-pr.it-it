---
description: Per abilitare il trasferimento dei file dell'applicazione, COMREPL gestisce automaticamente i set di cartelle file system nell'origine e nella destinazione. Queste cartelle di COMREPL sono tutte radicate nella replica% systemdir% \\ com \\ .
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gestione file (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523426"
---
# <a name="file-management"></a>Gestione dei file

Per abilitare il trasferimento dei file dell'applicazione, COMREPL gestisce automaticamente i set di cartelle file system nell'origine e nella destinazione. Queste cartelle di COMREPL sono tutte radicate nella replica% systemdir% \\ com \\ .

## <a name="source-folders"></a>Cartelle di origine



| Cartella                   | Scopo                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Le applicazioni esportate durante la fase di preparazione vengono archiviate qui.<br/> Questa cartella viene sovrascritta ogni volta che la fase di preparazione viene eseguita su un computer di origine specifico. Questa cartella non viene mai eliminata in modo esplicito, quindi la replica sulle destinazioni può avvenire in qualsiasi momento dopo la preparazione dell'origine.<br/> Ogni applicazione viene archiviata nella propria sottocartella denominata <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Cartelle di destinazione



| Cartella                    | Scopo                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | La fase di copia copia tutti i file e le sottocartelle da ReplicaSource nell'origine in ReplicaNew nella destinazione. Qualsiasi contenuto precedente di ReplicaNew viene eliminato ogni volta che la fase di copia viene eseguita su una determinata destinazione.<br/> Questa cartella esiste solo durante l'esecuzione del processo di replica. Vedere ReplicaCurrent.<br/>           |
| ReplicaCurrent<br/> | Le applicazioni replicate attualmente installate nella destinazione vengono archiviate qui.<br/> Quando viene avviata la fase di installazione, la cartella ReplicaNew viene rinominata ReplicaCurrent. Se è presente una cartella ReplicaCurrent esistente, viene rinominata in ReplicaOld. Se è presente una cartella ReplicaOld esistente, il relativo contenuto viene eliminato.<br/> |
| ReplicaOld<br/>     | Salva i file dell'applicazione installati durante il prossimo all'ultima replica. Questi file vengono salvati solo a scopo di backup.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> <dt>

[Cosa viene replicato](what-gets-replicated.md)
</dt> </dl>

 

 




