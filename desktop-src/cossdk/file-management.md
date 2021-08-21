---
description: Per abilitare il trasferimento dei file dell'applicazione, COMREPL gestisce automaticamente i set file system cartelle nell'origine e nella destinazione. Queste cartelle COMREPL sono tutte radice nella replica %systemdir% \\ \\ com.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gestione file (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685287e783dc5ae45d564897a37733568cc150d9af43322d5f435100e8f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307316"
---
# <a name="file-management"></a>Gestione dei file

Per abilitare il trasferimento dei file dell'applicazione, COMREPL gestisce automaticamente i set file system cartelle nell'origine e nella destinazione. Queste cartelle COMREPL sono tutte radice nella replica %systemdir% \\ \\ com.

## <a name="source-folders"></a>Cartelle di origine



| Cartella                   | Scopo                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Le applicazioni esportate durante la fase di preparazione vengono archiviate qui.<br/> Questa cartella viene sovrascritta ogni volta che viene eseguita la fase di preparazione in un determinato computer di origine. Questa cartella non viene mai eliminata in modo esplicito, quindi la replica alle destinazioni può essere verificata in qualsiasi momento dopo la preparazione dell'origine.<br/> Ogni applicazione viene archiviata nella propria sottocartella denominata <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Cartelle di destinazione



| Cartella                    | Scopo                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNuovo<br/>     | La fase di copia copia tutti i file e le sottocartelle da ReplicaSource nell'origine a ReplicaNuovo nella destinazione. Tutti i contenuti precedenti di ReplicaNew vengono eliminati ogni volta che la fase di copia viene eseguita su una determinata destinazione.<br/> Questa cartella esiste solo durante l'esecuzione del processo di replica. Vedere ReplicaCurrent.<br/>           |
| ReplicaCurrent<br/> | Le applicazioni replicate attualmente installate nella destinazione vengono archiviate qui.<br/> Quando viene avviata la fase di installazione, la cartella ReplicaNuovo viene rinominata in ReplicaCurrent. Se è presente una cartella ReplicaCurrent esistente, viene rinominata ReplicaOld. Se è presente una cartella ReplicaOld esistente, il relativo contenuto viene eliminato.<br/> |
| ReplicaOld<br/>     | Salva i file dell'applicazione installati durante l'ultima replica. Questi file vengono salvati solo a scopo di backup.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> <dt>

[Elementi replicati](what-gets-replicated.md)
</dt> </dl>

 

 




